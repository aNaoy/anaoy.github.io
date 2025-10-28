---
title: 'Crypto wasted: BlueNoroff’s ghost mirage of funding and jobs'
date: 2025-10-28
permalink: /posts/2025/10/28/crypto-wasted-bluenoroffs-ghost-mirage-of-funding-and-jobs/
tags:
- veille-cyber
- securelist
---
## La menace BlueNoroff : des tactiques sophistiquées pour le gain financier

Le groupe de cybercriminalité BlueNoroff, également connu sous d'autres noms, continue de cibler des individus et des entreprises du secteur de la blockchain et des cryptomonnaies dans le cadre de son opération "SnatchCrypto". Deux campagnes récentes, baptisées **GhostCall** et **GhostHire**, révèlent des méthodes d'attaque évoluées, exploitant des techniques d'ingénierie sociale avancées et l'intelligence artificielle.

### Points Clés :

*   **Ciblage d'élite :** BlueNoroff vise des développeurs blockchain, des cadres supérieurs et des gestionnaires dans l'industrie Web3/crypto.
*   **Ingénierie sociale complexe :** Les attaques reposent sur la tromperie, imitant des investisseurs, des recruteurs ou des employés légitimes.
*   **Utilisation de l'IA :** L'intelligence artificielle est employée pour améliorer la création de contenu, l'embellissement d'images et potentiellement la génération de scripts malveillants, augmentant ainsi l'efficacité et la furtivité des attaques.
*   **Multiplateforme :** Les campagnes ciblent à la fois les systèmes macOS et Windows, avec des malwares adaptés à chaque système d'exploitation.
*   **Vol de données étendu :** Au-delà des informations financières, le groupe cherche à collecter des données sensibles sur l'infrastructure, les outils de collaboration, les identifiants et les communications personnelles.

### Campagne GhostCall :

Cette campagne cible principalement les utilisateurs de macOS en les contactant via Telegram pour les inviter à de fausses réunions d'investissement. Les victimes sont conduites sur de faux sites web imitant des plateformes de visioconférence, où de véritables enregistrements d'autres victimes sont diffusés pour simuler une réunion réelle. Un faux message d'alerte incite ensuite l'utilisateur à mettre à jour un client ou un SDK, déclenchant le téléchargement et l'exécution de scripts malveillants.

*   **Méthode d'accès initiale :** Contact via Telegram, usurpation d'identité de capital-risqueurs, utilisation de faux liens de réunion Zoom/Teams.
*   **Déclenchement du malware :** Incitation à télécharger une fausse mise à jour Zoom/Teams (AppleScript sur macOS, technique ClickFix sur Windows).
*   **Composants malveillants observés :**
    *   **ZoomClutch/TeamsClutch :** Fausses applications Zoom/Teams dérobant des identifiants.
    *   **DownTroy :** Chaînes d'infection multiples incluant des téléchargeurs et des stealer (keyloggers, collecteurs d'informations).
    *   **CosmicDoor :** Malware polyglotte (Rust, Python, Nim, Go) communiquant via WSS, permettant le contrôle à distance.
    *   **SilentSiphon :** Suite de scripts de vol de données ciblant les notes, les extensions de navigateur, les identifiants, les secrets de développement et les données Telegram.
    *   **RooTroy :** Chaîne d'infection multi-composants (installateur, loader, injector) résultant en un backdoor Go.
    *   **RealTimeTroy :** Backdoor Go communiquant via WSS, avec des capacités d'injection de code.
    *   **SneakMain :** Malware Nim/Rust collectant des informations système et exécutant des commandes à distance.
    *   **SysPhon :** Downloader C++, potentiellement utilisé pour déployer d'autres malwares comme KANDYKORN.

### Campagne GhostHire :

Cette campagne, moins visible mais tout aussi dangereuse, cible les développeurs et ingénieurs par le biais de fausses offres d'emploi. Les acteurs de la menace se font passer pour des recruteurs et utilisent Telegram pour contacter les victimes, les incitant à télécharger un projet de "test de compétences" hébergé sur GitHub ou via un bot Telegram. Ce projet, souvent un simulateur de transaction de cryptomonnaies, contient des dépendances malveillantes ou du code embarqué qui, une fois exécuté, télécharge des malwares multiplateformes (Windows, Linux, macOS).

*   **Méthode d'accès initiale :** Contact via Telegram, usurpation d'identité de recruteurs, fausses offres d'emploi, liens vers de faux profils LinkedIn.
*   **Déclenchement du malware :** Exécution de projets de codage malveillants contenant des dépendances infectées ou du code intégré.
*   **Composants malveillants observés :**
    *   **DownTroy :** Téléchargeur multiplateforme (PowerShell, bash, AppleScript) servant à récupérer d'autres malwares.
    *   **Paquets Go malveillants :** Des dépôts officiels de packages Go ont été compromis pour héberger des dépendances malveillantes (ex: `uniroute`, `sorttemplate`).
    *   **Projet TypeScript malveillant :** Un projet Next.js sur GitHub contient du code JavaScript/TypeScript malveillant pour télécharger des charges utiles.

### Vulnérabilités et Exploits :

Bien que l'article ne détaille pas de CVEs spécifiques pour des vulnérabilités logicielles directement exploitées, les tactiques utilisées reposent sur l'exploitation des éléments suivants :

*   **Ingénierie sociale :** Tromperie pour inciter les victimes à télécharger et exécuter des fichiers malveillants.
*   **TCC (Transparency, Consent, and Control) Bypass sur macOS :** Manipulation de la base de données TCC pour obtenir des permissions d'accès non autorisées.
*   **UAC Bypass sur Windows :** Utilisation de techniques connues (RPC-based UAC bypass) pour élever les privilèges.
*   **Injection de processus :** Techniques permettant d'exécuter du code malveillant dans des processus légitimes.
*   **Modification/Corruption de PE Header :** Techniques pour rendre l'analyse des payloads plus difficile.

### Recommandations :

*   **Vigilance face aux communications suspectes :** Être particulièrement prudent avec les offres d'emploi, les invitations à des réunions et les demandes de téléchargement, surtout si elles proviennent de sources inconnues ou non vérifiées.
*   **Vérification des sources :** Toujours vérifier l'authenticité des contacts, des profils et des liens avant de cliquer ou de télécharger quoi que ce soit.
*   **Sécurité des systèmes :** Maintenir les systèmes d'exploitation et les logiciels à jour avec les derniers correctifs de sécurité.
*   **Utilisation de solutions de sécurité robustes :** Déployer et maintenir à jour des antivirus et des solutions de détection et de réponse (EDR) performantes.
*   **Formation à la cybersécurité :** Sensibiliser régulièrement les employés aux techniques d'ingénierie sociale et aux risques en ligne.
*   **Gestion des identifiants :** Utiliser des mots de passe forts et uniques, et envisager l'authentification multi-facteurs lorsque cela est possible.
*   **Surveillance des journaux d'événements :** Examiner les journaux système pour détecter toute activité suspecte.

---
[Source](https://securelist.com/bluenoroff-apt-campaigns-ghostcall-and-ghosthire/117842/){:target="_blank"}
