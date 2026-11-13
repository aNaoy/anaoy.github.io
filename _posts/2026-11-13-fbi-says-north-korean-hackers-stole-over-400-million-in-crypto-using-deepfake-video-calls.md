---
title: 'FBI Says North Korean Hackers Stole Over $400 Million in Crypto Using Deepfake Video Calls'
date: 2026-11-13
permalink: /posts/2026/11/13/fbi-says-north-korean-hackers-stole-over-400-million-in-crypto-using-deepfake-video-calls/
tags:
- veille-cyber
- hackernews
---
### FaceStealer : La campagne de cyberespionnage et de vol de cryptomonnaies nord-coréenne

Le groupe nord-coréen BlueNoroff (aussi connu sous le nom d'APT38) a orchestré une campagne sophistiquée baptisée **FaceStealer**, responsable du vol de plus de 400 millions de dollars en cryptomonnaies sur les 18 derniers mois. Cette opération cible principalement les cadres dirigeants et les développeurs des secteurs de la blockchain et du Web3.

**Points clés de l'attaque :**
*   **Ingénierie sociale avancée :** Utilisation de comptes compromis pour inviter les cibles à des réunions vidéo (Zoom, Teams).
*   **Deepfakes et usurpation :** Les attaquants utilisent des vidéos enregistrées, des deepfakes générés par IA et des photos de profil synthétiques pour gagner la confiance des victimes.
*   **Le leurre "ClickFix" :** Sous prétexte d'un problème technique lors de l'appel, la cible est incitée à cliquer sur un lien malveillant ou à exécuter un script, entraînant l'installation de malwares permettant le vol de cryptomonnaies et de privilèges d'accès.
*   **Propagation virale :** Une fois le poste de travail infecté, les attaquants prennent le contrôle des comptes de messagerie et de réseaux sociaux de la victime pour cibler ses contacts professionnels.

**Vulnérabilités et vecteurs d'infection :**
*   **VS Code :** Utilisation malveillante de fichiers de configuration `tasks.json` pour exécuter des scripts lors de l'ouverture d'un projet.
*   **Git Hooks :** Exploitation des scripts `.githooks` (pre-commit/post-checkout) pour déclencher l'exécution de code malveillant dès la manipulation de dépôts de code.
*   **Logiciels "trojanisés" :** Distribution de malwares (ex: *BeaverTail*, *InvisibleFerret*) via des outils utilitaires macOS piégés ou des tests techniques de recrutement fictifs.
*   *Note : Les techniques décrites exploitent le manque de méfiance humaine face à des outils de communication de confiance plutôt qu'une vulnérabilité CVE spécifique dans les logiciels de visioconférence.*

**Recommandations de sécurité :**
*   **Environnements isolés :** Exécuter systématiquement tout test technique ou code reçu dans des machines virtuelles (VM) éphémères, jamais sur un poste de travail professionnel.
*   **Vigilance accrue sur le recrutement :** Se méfier des processus d'entretien exigeant l'exécution de code ou le partage d'écran pour installer des dépendances, même via des recruteurs possédant des badges de vérification sur LinkedIn.
*   **Vérification des sources :** Contrôler rigoureusement la création des profils des recruteurs et la cohérence des informations sur les sites officiels des entreprises.
*   **Politiques de sécurité :** Les entreprises doivent instaurer des règles strictes interdisant l'exécution de fichiers provenant de sources externes non validées par les équipes de cybersécurité.

---
[Source](https://thehackernews.com/2026/11/fbi-says-north-korean-hackers-stole.html){:target="_blank"}
