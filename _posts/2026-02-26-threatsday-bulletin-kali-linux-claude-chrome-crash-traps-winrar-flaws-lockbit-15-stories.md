---
title: 'ThreatsDay Bulletin: Kali Linux + Claude, Chrome Crash Traps, WinRAR Flaws, LockBit & 15+ Stories'
date: 2026-02-26
permalink: /posts/2026/02/26/threatsday-bulletin-kali-linux-claude-chrome-crash-traps-winrar-flaws-lockbit-15-stories/
tags:
- veille-cyber
- hackernews
---
### Tendances Récentes en Cybersécurité : Accélération des Attaques et Nouvelles Méthodes d'Infiltration

L'écosystème de la cybersécurité observe une accélération notable des tactiques d'attaque et une sophistication accrue des méthodes d'infiltration. Les attaquants exploitent de plus en plus des techniques dissimulées, rendant la détection et la réponse plus difficiles.

**Points Clés et Vulnérabilités :**

*   **IA et Automatisation :** L'intégration de l'intelligence artificielle dans les opérations malveillantes permet une réduction drastique des temps d'attaque, notamment pour la progression latérale (29 minutes en moyenne) et l'exfiltration de données. Des groupes comme Fancy Bear, Akira, et Blind Eagle utilisent l'IA pour optimiser leurs attaques.
*   **Vol de Données et Spyware :**
    *   Des campagnes de **phishing** ciblent les services de crypto-monnaies, demandant la reconfirmation d'informations sensibles pour voler identifiants et données personnelles.
    *   Un spyware **Android**, **ResidentBat**, attribué aux autorités biélorusses, cible des journalistes et membres de la société civile pour des opérations de surveillance, collectant logs d'appels, enregistrements audio, SMS, et fichiers locaux.
    *   Des extensions **Chrome** malveillantes, comme Pixel Shield et PageGuard, ainsi que des campagnes "ClickFix", provoquent un crash du navigateur pour inciter les utilisateurs à exécuter des commandes dangereuses.
    *   Des campagnes de **malvertising** via Google Ads ciblent les utilisateurs Mac recherchant des logiciels populaires, les redirigeant vers des sites frauduleux pour installer le logiciel voleur de données **MacSync** ou d'autres malwares de type ClickFix.
    *   Le groupe Silver Fox utilise le **typosquatting** (sites web ressemblant à des antivirus légitimes) pour distribuer le RAT **ValleyRAT**.
    *   Une campagne de **repo-squatting** sur GitHub, utilisant des publicités sponsorisées, distribue les chargeurs **Hijack Loader** et le voleur **Atomic Stealer** pour Windows et macOS.
*   **Exploitation de Logiciels Obsolètes :**
    *   Une proportion écrasante de réseaux informatiques utilise des versions de **WinRAR** vulnérables à la faille **CVE-2025-8088**, largement exploitée.
    *   Des serveurs **Apache ActiveMQ** exposés sur Internet sont ciblés via la faille **CVE-2023-46604**, utilisée pour déployer le ransomware **LockBit**.
*   **Nouvelles Méthodes d'Attaque :**
    *   **Kali Linux** intègre l'IA avec Claude pour exécuter des commandes en langage naturel.
    *   Des campagnes de **spear-phishing** ciblent le secteur judiciaire argentin, livrant un RAT basé sur Rust via un fichier ZIP trompeur.
    *   Des **réunions Microsoft Teams** sont utilisées pour distribuer des malwares macOS, dans le cadre d'attaques attribuées à la Corée du Nord (GhostCall).
*   **Risques Cryptographiques :** De nombreux projets open-source (plus de 723 000) utilisent des bibliothèques cryptographiques avec des défauts de sécurité, notamment des réutilisations de vecteurs d'initialisation (IV) dans des algorithmes comme AES-CTR, ce qui peut compromettre la sécurité des données chiffrées (mention de **CVE-2026-25998** pour strongMan).
*   **Déclin de Forums Criminels :** La saisie du forum **RAMP** a déstabilisé l'écosystème underground, entraînant une redistribution des acteurs sur diverses plateformes, signe d'adaptation plutôt que de déclin.
*   **Évolution des Techniques :** L'utilisation de la clandestinité et de l'exploitation de la confiance (via de faux documents judiciaires ou des invitations de réunion) est en augmentation.

**Recommandations :**

*   **Mises à Jour Immédiates :** Appliquer rapidement les correctifs pour les logiciels critiques, tels que WinRAR (CVE-2025-8088) et Apache ActiveMQ (CVE-2023-46604).
*   **Vigilance Renforcée :** Être extrêmement prudent face aux e-mails, invitations, publicités et mises à jour logicielles inattendues.
*   **Gestion des Identifiants :** Mettre en œuvre des mesures de sécurité robustes pour protéger les identifiants légitimes, qui sont de plus en plus la porte d'entrée principale des attaquants.
*   **Sécurité des Extensions et Applications :** Examiner attentivement les permissions demandées par les extensions de navigateur et les applications, et se méfier des sources non officielles pour les téléchargements.
*   **Sensibilisation à l'IA :** Comprendre que l'IA est un outil puissant utilisé par les attaquants pour améliorer leurs capacités.
*   **Audits de Sécurité :** Utiliser des outils d'audit de sécurité, y compris des solutions basées sur l'IA, pour détecter et corriger les vulnérabilités, notamment dans les smart contracts (mention d'EVMbench).
*   **Protection contre le Phishing et le Malvertising :** Utiliser des solutions de sécurité robustes et former les utilisateurs à reconnaître les signes de phishing et les publicités malveillantes.
*   **Surveillance du Réseau :** Mettre en place une surveillance accrue, en particulier pour les périphériques périphériques qui manquent souvent d'une supervision complète.

La rapidité croissante des attaques, la sophistication des méthodes de tromperie et la capacité des attaquants à se fondre dans des activités quotidiennes normales exigent une vigilance constante et une adaptation des stratégies de défense.

---
[Source](https://thehackernews.com/2026/02/threatsday-bulletin-kali-linux-claude.html){:target="_blank"}
