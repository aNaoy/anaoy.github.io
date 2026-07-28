---
title: 'AutoIT Payload Injector , (Tue, Jul 28th)'
date: 2026-07-28
permalink: /posts/2026/07/28/autoit-payload-injector-tue-jul-28th/
tags:
- veille-cyber
- sans-isc
---
### Analyse d'une campagne de distribution de malware via AutoIT

Cette analyse détaille une campagne de malwares exploitant l'interpréteur **AutoIT** pour injecter des charges utiles malveillantes dans des processus système légitimes.

**Points clés de l'infection :**
*   **Vecteur initial :** E-mails de phishing (prétexte bancaire) contenant une archive RAR.
*   **Chaîne d'exécution :**
    1. Un script VBS décode et exécute un script PowerShell.
    2. PowerShell déploie trois fichiers : l'interpréteur AutoIT3, un script AutoIT chiffré et un fichier contenant un shellcode chiffré (XOR).
    3. Persistance : Création d'une clé de registre `Run` dans `HKCU`.
    4. AutoIT exécute le script qui injecte le shellcode (VIPKeylogger) dans le processus légitime `charmap.exe` via des appels API Windows.
*   **Technique :** Utilisation des fonctions `DllCall` d'AutoIT pour invoquer directement des fonctions système (`OpenProcess`, `VirtualAllocEx`, `WriteProcessMemory`, `CreateRemoteThread`) afin d'effectuer une injection mémoire (Process Hollowing).

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est exploitée ; le malware détourne des fonctionnalités légitimes de Windows (AutoIT et API système) pour contourner les défenses. Il s'agit d'une technique de type **Living-off-the-Land (LotL)**.

**Recommandations :**
*   **Filtrage des emails :** Bloquer les archives RAR provenant de sources inconnues ou contenant des scripts (VBS, PowerShell).
*   **Contrôle des applications :** Restreindre l'exécution des binaires AutoIT dans les environnements professionnels via des solutions de type EDR/AppLocker.
*   **Surveillance système :** Surveiller les processus suspects (comme `charmap.exe`) qui établissent des connexions réseau sortantes ou qui sont créés par des scripts non signés.
*   **Analyse comportementale :** Configurer les alertes EDR pour détecter l'utilisation de `DllCall` par des scripts AutoIT, ainsi que les appels API de type `CreateRemoteThread` émanant de processus inhabituels.

---
[Source](https://isc.sans.edu/diary/rss/33192){:target="_blank"}
