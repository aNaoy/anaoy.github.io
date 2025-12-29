---
title: '⚡ Weekly Recap: MongoDB Attacks, Wallet Breaches, Android Spyware, Insider Crime & More'
date: 2025-12-29
permalink: /posts/2025/12/29/weekly-recap-mongodb-attacks-wallet-breaches-android-spyware-insider-crime-more/
tags:
- veille-cyber
- hackernews
---
## Vulnérabilités et Menaces Cyber de Fin 2025

La fin de l'année 2025 a été marquée par une multitude de failles de sécurité exploitées, souvent plus rapidement que les correctifs. Les accès légitimes ont été abusés et les conséquences de certaines attaques se sont fait sentir sur le long terme.

### Points Clés :

*   **Vitesse d'exploitation accrue :** Les vulnérabilités sont exploitées peu de temps après leur découverte.
*   **Abus d'accès :** Des accès destinés au travail, aux mises à jour ou au support ont été compromis.
*   **Impact différé :** Les dommages persistent parfois des mois, voire des années après l'incident initial.

### Vulnérabilités Principales et Exploitations Notées :

*   **CVE-2025-14847 (MongoDB) :** Une vulnérabilité critique (score CVSS de 8.7) permettant à un attaquant non authentifié de lire la mémoire du serveur MongoDB à distance. Connue sous le nom de "MongoBleed", elle a touché plus de 87 000 instances, dont 42% dans des environnements cloud.
    *   **Recommandation :** Mettre à jour vers les versions 8.2.3, 8.0.17, 7.0.28, 6.0.27, 5.0.32, et 4.4.30 de MongoDB.
*   **Extension Chrome Trust Wallet :** Un incident de sécurité a entraîné la perte d'environ 7 millions de dollars. Il semblerait qu'une version malveillante de l'extension (v2.68) ait été publiée via une clé API compromise de Chrome Web Store.
    *   **Recommandation :** Mettre à jour l'extension vers la version 2.69. Les utilisateurs mobile et d'autres navigateurs ne sont pas affectés.
*   **Evasive Panda (APT) :** Ce groupe lié à la Chine a utilisé des attaques par empoisonnement DNS pour distribuer son malware MgBot via des mises à jour falsifiées d'outils populaires (SohuVA, iQIYI Video, IObit Smart Defrag, Tencent QQ). L'activité s'est déroulée entre novembre 2022 et novembre 2024.
*   **Vol de crypto suite à la brèche LastPass 2022 :** Des attaquants ont réussi à compromettre des sauvegardes de coffres-forts chiffrés volés en 2022, exploitant des mots de passe maîtres faibles pour dérober plus de 35 millions de dollars en cryptomonnaies.
*   **CVE-2020-12812 (Fortinet SSL VPN) :** Une vulnérabilité plus ancienne, toujours activement exploitée dans certaines configurations, permettant une connexion sans authentification à deux facteurs si le nom d'utilisateur était modifié.
    *   **Recommandation :** Contacter le support Fortinet et réinitialiser toutes les informations d'identification en cas de preuve d'authentification sans 2FA.
*   **Faux package npm WhatsApp API :** Le package "lotusbail" a été téléchargé plus de 56 000 fois, permettant l'interception de messages, l'envoi de messages, le téléchargement de médias et l'accès aux listes de contacts. La déconnexion manuelle des appareils est nécessaire pour rompre le lien.
*   **Autres CVEs notables :** CVE-2025-68664 (LangChain Core), CVE-2023-52163 (Digiever DS-2105 Pro), CVE-2025-68613 (n8n), CVE-2025-13836 (Python http.client), CVE-2025-26794 (Exim), CVE-2025-68615 (Net-SNMP), CVE-2025-44016 (TeamViewer DEX Client), CVE-2025-13008 (M-Files Server).
*   **LANDFALL (Spyware Android) :** Exploite une faille zero-day (CVE-2025-21042) sur les appareils Samsung Galaxy, via des fichiers d'image DNG envoyés potentiellement par WhatsApp, affectant la bibliothèque Quram.
*   **ResidentBat (Spyware Android) :** Découvert sur les téléphones de journalistes biélorusses, il collecte des données sensibles, enregistre l'audio, prend des captures d'écran et peut effectuer une réinitialisation d'usine. Son installation nécessite un accès physique.
*   **CVE-2025-54068 (Livewire) :** Une faille critique (score CVSS de 9.8) permettant l'exécution de commandes à distance, même sans connaissance de la clé `APP_KEY` dans certains cas.
    *   **Recommandation :** Mettre à jour vers la version 3.6.4 de Livewire.

### Recommandations Générales :

*   **Mises à jour régulières :** Appliquer les correctifs de sécurité dès leur disponibilité, notamment pour MongoDB, Trust Wallet, Fortinet, Livewire, et d'autres logiciels critiques.
*   **Surveillance des accès :** Redoubler de vigilance sur les accès légitimes et les comptes d'administrateur.
*   **Authentification forte :** Utiliser l'authentification à deux facteurs (2FA) partout où c'est possible.
*   **Vérification des sources :** Faire preuve de prudence avec les packages de dépôts publics (npm) et les extensions de navigateur.
*   **Conscience des risques :** Être conscient des techniques d'ingénierie sociale (fausses offres d'emploi) et de l'exploitation des vulnérabilités zero-day.
*   **Sécurité des appareils :** Soyez vigilant quant à la confiscation d'appareils et aux risques d'installation de logiciels espions.

---
[Source](https://thehackernews.com/2025/12/weekly-recap-mongodb-attacks-wallet.html){:target="_blank"}
