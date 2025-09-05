---
title: 'VirusTotal Finds 44 Undetected SVG Files Used to Deploy Base64-Encoded Phishing Pages'
date: 2025-09-05
permalink: /posts/2025/09/05/virustotal-finds-44-undetected-svg-files-used-to-deploy-base64-encoded-phishing-pages/
tags:
- veille-cyber
- hackernews
---
## Campagne de Phishing Sophistiquée Utilise des Fichiers SVG Inconnus

Une nouvelle campagne de logiciels malveillants utilise des fichiers Scalable Vector Graphics (SVG) pour diffuser des pages de phishing déguisées en documents officiels du système judiciaire colombien. Ces fichiers SVG, distribués par e-mail, contiennent un code JavaScript embarqué qui décode et injecte une page HTML de phishing encodée en Base64. Cette fausse page simule le téléchargement d'un document officiel tout en déclenchant discrètement le téléchargement d'une archive ZIP.

VirusTotal a identifié 44 fichiers SVG uniques indétectables par les moteurs antivirus, grâce à des techniques d'obfuscation, de polymorphisme et l'ajout de code superflu pour échapper à la détection statique. Au total, 523 fichiers SVG ont été repérés, le plus ancien datant d'août 2025. Les chercheurs ont observé une diminution de la taille des fichiers au fil du temps, suggérant une évolution des charges utiles par les attaquants.

Parallèlement, des versions crackées de logiciels et des tactiques de type "ClickFix" sont exploitées pour infecter les systèmes macOS avec le voleur d'informations Atomic macOS Stealer (AMOS). AMOS est conçu pour voler des identifiants, des données de navigation, des portefeuilles de cryptomonnaies, des conversations Telegram et d'autres informations sensibles. Les attaques ciblent les utilisateurs recherchant des logiciels piratés, les redirigeant vers de faux liens de téléchargement qui incitent à exécuter des commandes malveillantes via l'application Terminal. Bien que les protections Gatekeeper de macOS bloquent l'installation de fichiers .dmg non signés, les attaquants s'adaptent en utilisant des méthodes d'installation basées sur le Terminal pour contourner les contrôles de sécurité.

Une autre campagne majeure cible les joueurs à la recherche de triches pour jeux vidéo, distribuant le malware StealC et des logiciels de vol de cryptomonnaies, générant plus de 135 000 dollars pour les acteurs malveillants. StealC est capable de télécharger des charges utiles supplémentaires, y compris un voleur d'actifs numériques.

### Points Clés :

*   Utilisation de fichiers SVG comme vecteur d'attaque pour le phishing.
*   Injection de pages de phishing encodées en Base64.
*   Évasion des antivirus grâce à des techniques d'obfuscation avancées.
*   Campagne AMOS ciblant les utilisateurs macOS via des logiciels piratés et des méthodes d'installation via Terminal.
*   Campagne StealC visant les joueurs avec des malwares de vol d'informations et de cryptomonnaies.

### Vulnérabilités :

*   Aucune CVE spécifique n'est mentionnée dans l'article pour les fichiers SVG. La vulnérabilité réside dans la capacité des fichiers SVG à exécuter du code JavaScript malveillant et dans l'exploitation de la confiance des utilisateurs dans les documents officiels ou les logiciels.
*   Pour AMOS, l'exploitation réside dans la confiance des utilisateurs dans les sources de téléchargement de logiciels piratés et dans le contournement des protections par défaut de macOS via des commandes Terminal.

### Recommandations :

*   **Vigilance face aux e-mails suspects :** Ne pas cliquer sur les liens ou télécharger les pièces jointes provenant d'expéditeurs inconnus ou dont l'authenticité est douteuse.
*   **Vérification des fichiers :** Examiner attentivement l'origine et le contenu des fichiers téléchargés, même ceux qui semblent légitimes.
*   **Utilisation d'antivirus à jour :** Maintenir à jour les logiciels de sécurité et effectuer des analyses régulières.
*   **Prudence avec les logiciels piratés :** Éviter le téléchargement et l'installation de logiciels provenant de sources non officielles.
*   **Mises à jour du système d'exploitation et des logiciels :** Appliquer les correctifs de sécurité dès qu'ils sont disponibles pour pallier les vulnérabilités connues.
*   **Stratégies de défense en profondeur :** Ne pas se fier uniquement aux protections intégrées du système d'exploitation, mais adopter une approche multicouche de la sécurité.
*   **Sensibilisation des utilisateurs :** Informer régulièrement les utilisateurs sur les menaces actuelles et les bonnes pratiques de cybersécurité.

---
[Source](https://thehackernews.com/2025/09/virustotal-finds-44-undetected-svg.html){:target="_blank"}
