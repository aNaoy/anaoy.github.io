---
title: 'Cloud Atlas activity in the second half of 2025 and early 2026: new tools and a new payload'
date: 2026-05-22
permalink: /posts/2026/05/22/cloud-atlas-activity-in-the-second-half-of-2025-and-early-2026-new-tools-and-a-new-payload/
tags:
- veille-cyber
- securelist
---
### Analyse des activités du groupe Cloud Atlas (2025-2026)

Le groupe APT **Cloud Atlas** a intensifié ses opérations entre fin 2025 et début 2026, ciblant principalement des entités gouvernementales et diplomatiques en Russie et en Biélorussie. Le groupe continue d'évoluer en intégrant des outils publics légitimes (Tor, SSH, RevSocks) pour masquer ses activités et assurer une persistance robuste.

#### Points clés
*   **Vecteur d'infection :** Phishing via des archives ZIP contenant des fichiers LNK malveillants exécutant des scripts PowerShell.
*   **Techniques de persistance :** Utilisation de clés de registre "Run" et de tâches planifiées Windows.
*   **Mouvement latéral et exfiltration :** Patching de `termsrv.dll` pour permettre des sessions RDP multiples, usage de `PowerCloud` pour exfiltrer des données vers Google Sheets, et vol d'identifiants Active Directory via "Kerberoasting" et accès aux fichiers SAM/SECURITY.
*   **Contournement :** Utilisation de tunnels SSH inversés, du réseau Tor pour l'accès RDP distant, et de versions modifiées d'OpenSSH pour échapper à la détection EDR.

#### Vulnérabilités exploitées
*   **CVE-2018-0802 :** Vulnérabilité dans l'éditeur d'équations de Microsoft Office utilisée pour le téléchargement et l'exécution de code malveillant.
*   **UAC Bypass :** Utilisation de l'utilitaire système `fodhelper.exe` pour élever les privilèges des scripts PowerShell.

#### Recommandations
1.  **Surveillance des processus :** Détecter l'exécution suspecte de scripts PowerShell initiée par des fichiers LNK ou des documents Office.
2.  **Gestion des accès :** Restreindre l'utilisation des outils de tunneling (SSH, RevSocks, Tor) au sein du réseau d'entreprise.
3.  **Durcissement RDP :** Surveiller toute modification suspecte de `termsrv.dll` et limiter le nombre de sessions RDP simultanées via GPO.
4.  **Analyse comportementale :** Surveiller les accès anormaux aux fichiers sensibles (`SAM`, `SECURITY`) et les tentatives d'exécution de `taskkill.exe` ciblant des utilitaires d'extraction.
5.  **Mises à jour :** Appliquer les correctifs pour les vulnérabilités Office anciennes et s'assurer que les politiques de contrôle d'exécution des scripts (PowerShell) sont strictement appliquées.

---
[Source](https://securelist.com/cloud-atlas-2026/119895/){:target="_blank"}
