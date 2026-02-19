---
title: 'Arkanix Stealer: a C++ & Python infostealer'
date: 2026-02-19
permalink: /posts/2026/02/19/arkanix-stealer-a-c-python-infostealer/
tags:
- veille-cyber
- securelist
---
## Arkanix Stealer : Une Menace Polymorphe et Modulaire

Arkanix Stealer est un logiciel malveillant de type "infostealer" apparu en octobre 2025, proposé sous un modèle de "malware-as-a-service" (MaaS). Il est disponible en versions C++ et Python, offrant une large gamme de fonctionnalités pour voler des informations sensibles. Sa promotion sur des forums spécialisés, l'utilisation de Discord pour la communication et l'intégration de fonctionnalités telles qu'un programme de parrainage le distinguent des malwares plus discrets.

### Points Clés

*   **Modèle MaaS :** Arkanix Stealer était proposé en tant que service, incluant l'implant, un panneau de contrôle configurable et des statistiques.
*   **Implants doubles :** L'offre comprenait une version C++ native et une version Python, chacune avec des spécificités.
*   **ChromElevator inclus :** La version C++ intégrait l'outil d'exploitation post-infection de navigateur "ChromElevator".
*   **Développement potentiellement assisté par IA :** Des indices dans le code suggèrent l'utilisation d'outils d'aide au développement, réduisant potentiellement le temps et les coûts de création.
*   **Campagne limitée :** L'infrastructure et le programme d'affiliation semblent avoir été rapidement désactivés après leur lancement, suggérant une campagne axée sur des gains rapides.
*   **Ciblage varié :** Le malware cible des informations relatives aux cryptomonnaies, aux jeux vidéo, à la navigation web, aux messageries et aux données système.

### Vulnérabilités et Points d'Intérêt

Bien que l'article ne détaille pas de vulnérabilités spécifiques exploitées par Arkanix Stealer lui-même, sa nature de "stealer" repose sur l'exploitation des données stockées légitimement par les applications et les systèmes d'exploitation. Les points d'intérêt technologiques incluent :

*   **Version Python :**
    *   Utilisation du module `subprocess` pour installer des dépendances (`requests`, `pycryptodome`, `psutil`, `pywin32`).
    *   Exécution dynamique de la configuration depuis le serveur de commande et contrôle (C2).
    *   Récupération d'informations système (OS, CPU, GPU, RAM, résolution d'écran, disposition clavier, fuseau horaire, logiciels installés, antivirus, VPN).
    *   Extraction de données de 22 navigateurs, y compris l'historique, l'autocomplétion, les mots de passe enregistrés et les cookies.
    *   Collecte de données Telegram (dossier `tdata`).
    *   Vol d'identifiants Discord et auto-propagation via l'API Discord.
    *   Recherche de logiciels VPN connus pour voler des identifiants.
    *   Exfiltration de fichiers basés sur des chemins prédéfinis et des extensions spécifiques (documents, médias), incluant des termes français.
    *   Téléchargement et exécution de modules additionnels : Chrome grabber, Wallet patcher (pour Exodus et Atomic), Extra collector (incluant la collecte de fichiers FileZilla, données VPN, Steam, captures d'écran), et HVNC.
    *   Déchiffrement des modules additionnels via AES-GCM et PBKDF2.
*   **Version C++ :**
    *   Utilisation de VMProtect et de contre-mesures anti-analyse (anti-VM, anti-debug).
    *   Patching de `AmsiScanBuffer` et `EtwEventWrite` pour contourner les protections système.
    *   Collecte d'informations sur les connexions RDP.
    *   Vol d'identifiants de plateformes de jeux populaires (Steam, Epic Games, Riot, etc.).
    *   Capture de captures d'écran.
    *   Exécution de ChromElevator à partir des ressources, avec injection directe dans les processus de navigateur via des syscalls.
    *   Chiffrement des communications avec le C2 via AES-GCM et PBKDF2.

Il n'y a pas de CVEs spécifiques mentionnés dans l'article pour des vulnérabilités exploitées par Arkanix Stealer lui-même.

### Recommandations

Les recommandations générales pour se prémunir contre ce type de menace incluent :

*   **Sensibilisation au phishing :** Être vigilant face aux courriels, messages et liens suspects qui pourraient être des vectimes d'infection.
*   **Mises à jour régulières :** Maintenir le système d'exploitation, les navigateurs et les logiciels de sécurité à jour pour bénéficier des derniers correctifs de sécurité.
*   **Logiciels de sécurité robustes :** Utiliser et maintenir à jour des solutions antivirus et anti-malware fiables. Les produits Kaspersky détectent cette menace sous les noms : `Trojan-PSW.Win64.Coins.*`, `HEUR:Trojan-PSW.Multi.Disco.gen`, `Trojan.Python.Agent.*`.
*   **Gestion prudente des identifiants :** Utiliser des mots de passe forts et uniques pour chaque compte, et envisager l'utilisation d'un gestionnaire de mots de passe. Activer l'authentification à deux facteurs lorsque cela est possible.
*   **Prudence avec les sources non fiables :** Éviter de télécharger et d'exécuter des logiciels ou des scripts provenant de sources non vérifiées.
*   **Sauvegardes régulières :** Effectuer des sauvegardes régulières des données importantes pour pouvoir les restaurer en cas de compromission.

---
[Source](https://securelist.com/arkanix-stealer/119006/){:target="_blank"}
