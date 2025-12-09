---
title: 'Researchers Find Malicious VS Code, Go, npm, and Rust Packages Stealing Developer Data'
date: 2025-12-09
permalink: /posts/2025/12/09/researchers-find-malicious-vs-code-go-npm-and-rust-packages-stealing-developer-data/
tags:
- veille-cyber
- hackernews
---
## Extension malveillante : vol de données des développeurs

Deux extensions pour Visual Studio Code (VS Code), "BigBlack.bitcoin-black" et "BigBlack.codo-ai", ont été identifiées comme contenant des logiciels malveillants. Elles se présentaient comme un thème sombre premium et un assistant de codage IA, mais dissimulaient des fonctionnalités malveillantes. Ces extensions pouvaient télécharger des charges utiles supplémentaires, capturer des captures d'écran, voler des mots de passe Wi-Fi, lire le presse-papiers, et détourner des sessions de navigateur en exfiltrant les données vers un serveur contrôlé par l'attaquant.

Parallèlement, des paquets malveillants ont été découverts dans les écosystèmes Go, npm et Rust :

*   **Go :** Les paquets "github.com/bpoorman/uuid" et "github.com/bpoorman/uid" usurpait des bibliothèques de confiance pour exfiltrer des données vers un site de partage de texte.
*   **npm :** 420 paquets npm uniques, publiés sous un modèle de nommage cohérent incluant "elf-stats-*", contenaient du code pour exécuter un shell inversé et exfiltrer des fichiers.
*   **Rust :** La crate "finch-rust" usurpait l'outil légitime "finch" et servait de chargeur pour un logiciel malveillant de vol d'identifiants ("sha-rust").

**Points Clés :**

*   Des extensions VS Code malveillantes déguisées en outils légitimes ont été découvertes.
*   Ces extensions volent des données sensibles des développeurs, incluant des informations système, des identifiants, et des sessions de navigateur.
*   Des paquets malveillants similaires ont été trouvés dans les écosystèmes Go, npm et Rust, visant également le vol de données.
*   Les attaquants utilisent des techniques de typosquatting, d'usurpation d'identité et de séparation des fonctions malveillantes pour échapper à la détection.

**Vulnérabilités :**

*   Bien que des CVE spécifiques ne soient pas mentionnés dans l'article, la nature du vol de données et le détournement de sessions indiquent des vulnérabilités critiques au niveau de la sécurité des applications et des systèmes des développeurs.

**Recommandations :**

*   Soyez vigilant quant aux extensions et paquets que vous installez, même s'ils proviennent de marketplaces réputées.
*   Vérifiez attentivement la source et la réputation des outils de développement et des bibliothèques avant de les intégrer dans vos projets.
*   Maintenez vos environnements de développement à jour avec les derniers correctifs de sécurité.
*   Utilisez des solutions de sécurité pour surveiller les activités suspectes sur vos systèmes de développement.

---
[Source](https://thehackernews.com/2025/12/researchers-find-malicious-vs-code-go.html){:target="_blank"}
