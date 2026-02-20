---
title: 'Under the Hood of DynoWiper, (Thu, Feb 19th)'
date: 2026-02-20
permalink: /posts/2026/02/20/under-the-hood-of-dynowiper-thu-feb-19th/
tags:
- veille-cyber
- sans-isc
---
**Analyse du Malware Destructeur DynoWiper**

Une analyse technique du malware destructeur (wiper) DynoWiper, actif fin décembre 2025 et ciblant des entreprises du secteur énergétique polonais, révèle ses mécanismes d'action. Les investigations d'ESET Research et CERT Polska suggèrent un lien avec des acteurs étatiques russes, potentiellement le groupe APT Sandworm, connu pour ses cyberattaques contre l'Ukraine.

**Points Clés :**

*   **Détection et Initialisation :** Le malware, une version A de DynoWiper (SHA-256: 835b0d87ed2d49899ab6f9479cddb8b4e03f5aeb2365c50a51f9088dcede68d5), n'utilise pas d'obfuscation ou de packing sophistiqué. Il initialise un générateur de nombres pseudo-aléatoires Mersenne Twister (MT19937).
*   **Corruption de Données :** Le malware parcourt récursivement les disques logiques (fixes et amovibles) pour identifier et corrompre des fichiers. Il évite certains répertoires système critiques tels que "system32", "windows", "program files", "recycle.bin", "boot", "perflogs", "appdata" et "documents and settings". Pour chaque fichier ciblé, il efface ses attributs, écrit un bloc de données aléatoires de 16 octets au début, puis de manière pseudo-aléatoire à d'autres emplacements du fichier (jusqu'à 4096 fois pour les fichiers volumineux).
*   **Suppression de Données :** Après la phase de corruption, DynoWiper procède à la suppression effective des fichiers ciblés en utilisant la fonction `DeleteFileW()`.
*   **Clôture du Système :** Enfin, le malware obtient les privilèges nécessaires (`SeShutdownPrivilege`) pour forcer un redémarrage du système via `ExitWindowsEx()`.

**Vulnérabilités / Techniques Utilisées (Mapping MITRE ATT&CK) :**

*   **Discovery (TA0007) :**
    *   T1680: Local Storage Discovery
    *   T1083: File and Directory Discovery
*   **Defense Evasion (TA0005) :**
    *   T1222: File and Directory Permissions Modification (T1222.001: Windows File and Directory Permissions Modification)
    *   T1134: Access Token Manipulation
*   **Privilege Escalation (TA0004) :**
    *   T1134: Access Token Manipulation
*   **Impact (TA0040) :**
    *   T1485: Data Destruction
    *   T1529: System Shutdown/Reboot

**Recommandations (Implicites basées sur l'analyse) :**

Bien que l'article se concentre sur l'analyse technique, les informations fournies impliquent la nécessité des mesures de cybersécurité suivantes :

*   **Détection et Blocage des Malwares :** Utilisation de solutions antivirus et de systèmes de détection d'intrusion à jour pour identifier et bloquer des malwares comme DynoWiper.
*   **Surveillance des Activités Suspectes :** Mise en place d'une surveillance réseau et système pour détecter des comportements anormaux, tels que des accès massifs à des fichiers, des modifications de permissions non autorisées, ou des tentatives de privilèges élevés.
*   **Sauvegardes Régulières et Isolées :** Maintenir des sauvegardes de données fiables et isolées pour pouvoir restaurer les systèmes affectés par des attaques de destruction de données.
*   **Gestion des Vulnérabilités et Patch Management :** S'assurer que les systèmes sont à jour avec les derniers correctifs de sécurité pour réduire la surface d'attaque potentielle des acteurs malveillants.
*   **Formation et Sensibilisation :** Former le personnel aux bonnes pratiques de cybersécurité pour éviter les compromissions initiales.

---
[Source](https://isc.sans.edu/diary/rss/32730){:target="_blank"}
