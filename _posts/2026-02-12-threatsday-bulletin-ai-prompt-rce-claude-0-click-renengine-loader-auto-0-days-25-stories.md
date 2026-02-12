---
title: 'ThreatsDay Bulletin: AI Prompt RCE, Claude 0-Click, RenEngine Loader, Auto 0-Days & 25+ Stories'
date: 2026-02-12
permalink: /posts/2026/02/12/threatsday-bulletin-ai-prompt-rce-claude-0-click-renengine-loader-auto-0-days-25-stories/
tags:
- veille-cyber
- hackernews
---
**Cybercriminalité : Tactiques Évolutives et Exploits Discrets**

Les acteurs malveillants adoptent une stratégie axée sur l'exploitation d'outils et de vulnérabilités existants, privilégiant une approche discrète et persistante plutôt que des exploits flamboyants. L'objectif évolue vers une présence à long terme pour extraire de la valeur, brouillant les pistes entre cybercriminalité, espionnage et intrusions opportunistes.

**Points Clés :**

*   **Exploitation d'outils légitimes :** Les attaquants utilisent des logiciels de surveillance (Net Monitor) et des plateformes de gestion à distance (SimpleHelp) pour déployer des ransomwares, évitant ainsi la détection basée sur des malwares traditionnels.
*   **Attaques ciblées et avancées :** Taïwan est une cible privilégiée pour les groupes APT, servant de terrain d'essai pour des tactiques qui seront ensuite déployées ailleurs.
*   **Vol de données sophistiqué :** De nouveaux logiciels malveillants comme LTX Stealer et Marco Stealer se concentrent sur le vol d'informations sensibles, notamment des identifiants, des données de cryptomonnaies et des fichiers stockés dans des services cloud.
*   **Ingénierie sociale évoluée :** Des campagnes de phishing innovantes exploitent l'abus de flux d'authentification natifs (Telegram) ou des documents HTA pour contourner les protections.
*   **Vulnérabilités Zero-Click et RCE :** Des failles critiques existent dans des applications courantes (Notepad, Claude Desktop Extensions) et dans des systèmes complexes (Looker, Quest Desktop Authority), permettant une exécution de code à distance, parfois sans interaction utilisateur.
*   **Cybercriminalité financière :** Les escroqueries de type "pig butchering" continuent de causer des pertes financières considérables.
*   **Montée du ransomware axé sur le vol de données :** Des groupes comme Coinbase Cartel se spécialisent dans l'exfiltration de données avant le chiffrement.
*   **Nouveaux chargeurs de malware :** RenEngine Loader et Foxveil facilitent la distribution de malwares de seconde étape, souvent via des canaux détournés comme des installateurs de jeux piratés.
*   **Vulnérabilités dans les systèmes critiques :** Le secteur de l'énergie est particulièrement vulnérable aux cyberattaques exploitant des défauts de sécurité des appareils OT et des identifiants par défaut.
*   **Développement d'IA malveillante :** Le framework VoidLink, potentiellement développé à l'aide d'IA, cible les environnements cloud avec des capacités de persistance avancées.

**Vulnérabilités Identifiées :**

*   **CVE-2026-20841 (Windows Notepad) :** Injection de commandes permettant l'exécution de code à distance via des liens Markdown. Score CVSS : 8.8.
*   **CVE-2025-67813 (Quest Desktop Authority) :** Exécution de code à distance avec privilèges SYSTEM via un named pipe. Score CVSS : 5.3.
*   **Vulnérabilité Zero-Click RCE (Claude Desktop Extensions) :** Permet une exécution de code à distance silencieuse via des événements Google Calendar. Score CVSS : 10.0.
*   **CVE-2026-24061 (GNU InetUtils telnetd) :** Contournement d'authentification critique dans le démon Telnet.
*   **CVE-2025-12743 (Google Looker - "LookOut") :** Chaîne RCE via des remplacements de hooks Git et contournement d'autorisation via l'abus de connexion à la base de données interne. Score CVSS : 6.5.
*   **76 Zero-Days (Pwn2Own Automotive) :** Découvertes dans les systèmes d'infodivertissement embarqués, les chargeurs de véhicules électriques et les systèmes d'exploitation automobiles.

**Recommandations :**

*   **Appliquer les correctifs de sécurité :** Maintenir les systèmes et applications à jour, notamment pour les vulnérabilités comme celle de Notepad.
*   **Surveiller l'utilisation des outils légitimes :** Être vigilant quant à l'usage détourné de logiciels de gestion et de surveillance.
*   **Renforcer l'authentification et la gestion des accès :** Mettre en place des mesures robustes pour prévenir le vol de sessions et l'élévation de privilèges.
*   **Éduquer les utilisateurs :** Sensibiliser aux techniques d'ingénierie sociale, notamment les faux liens, les fausses invitations et les demandes d'approbation inhabituelles.
*   **Segmenter les réseaux et sécuriser les infrastructures critiques :** Protéger les environnements sensibles contre les accès non autorisés et les compromissions.
*   **Utiliser des solutions de sécurité avancées :** Déployer des outils capables de détecter les comportements anormaux et le "living-off-the-land" (utilisation de programmes légitimes par les attaquants).
*   **Mettre à jour les plans de réponse aux incidents :** Se préparer à réagir efficacement aux cyberattaques, en particulier dans le secteur des infrastructures critiques.

---
[Source](https://thehackernews.com/2026/02/threatsday-bulletin-ai-prompt-rce.html){:target="_blank"}
