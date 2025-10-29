---
title: '10 npm Packages Caught Stealing Developer Credentials on Windows, macOS, and Linux'
date: 2025-10-29
permalink: /posts/2025/10/29/10-npm-packages-caught-stealing-developer-credentials-on-windows-macos-and-linux/
tags:
- veille-cyber
- hackernews
---
## Camouflage Malveillant dans les Packages npm

Dix paquets npm, diffusés le 4 juillet 2025 et cumulés plus de 9 900 téléchargements, ont été identifiés comme des portes d'entrée pour un logiciel espion conçu pour dérober des informations sensibles sur Windows, macOS et Linux. Ces paquets, créés par des typosquats de bibliothèques populaires (comme `discord.js`, `ethers.js`, `react-router-dom`, `typescript`, `nodemon` et `zustand`), utilisent des techniques d'obfuscation sophistiquées pour masquer leur nature malveillante.

Lors de l'installation, ils affichent une fausse interface de type CAPTCHA et simulent une procédure normale, tout en collectant l'adresse IP de la victime avant de télécharger un chargeur malveillant plus conséquent. Ce dernier, empaqueté avec PyInstaller, est capable d'accéder aux identifiants stockés dans les trousseaux système, les navigateurs et les services d'authentification sur les trois principaux systèmes d'exploitation. Les données ainsi collectées sont compressées et envoyées à un serveur distant.

**Points Clés:**

*   **Nature de la menace:** Dix paquets npm malveillants conçus pour le vol d'identifiants.
*   **Plateformes ciblées:** Windows, macOS, Linux.
*   **Méthode d'infection:** Typosquatting de noms de paquets populaires et utilisation de hooks `postinstall`.
*   **Techniques d'évasion:** Quatre couches d'obfuscation du code, affichage d'un faux CAPTCHA, exécution dans une nouvelle fenêtre de terminal.
*   **Cible principale:** Identifiants stockés dans les trousseaux système, navigateurs, et fichiers de configuration.
*   **Volume:** Plus de 9 900 téléchargements cumulés pour les paquets malveillants.

**Paquets Malveillants Identifiés:**

*   deezcord.js
*   dezcord.js
*   dizcordjs
*   etherdjs
*   ethesjs
*   ethetsjs
*   nodemonjs
*   react-router-dom.js
*   typescriptjs
*   zustand.js

**Vulnérabilités:**

Aucun numéro CVE spécifique n'est mentionné dans l'article, mais la vulnérabilité réside dans la confiance accordée aux paquets tiers non vérifiés et à l'absence de vérification de leur légitimité avant l'installation. L'utilisation de hooks `postinstall` par des paquets non fiables est un vecteur d'attaque connu.

**Recommandations:**

*   **Vérification rigoureuse des paquets:** Examiner attentivement les noms des paquets et les sources avant de les installer, en particulier les dépendances. Se méfier des noms de paquets trop similaires aux bibliothèques populaires.
*   **Analyse des hooks `postinstall`:** Être attentif aux scripts qui s'exécutent automatiquement après l'installation d'un paquet.
*   **Maintien des systèmes à jour:** Bien que non directement lié à cette attaque, maintenir les systèmes d'exploitation et les environnements de développement à jour contribue à une sécurité globale renforcée.
*   **Surveillance des téléchargements:** Les équipes de sécurité devraient surveiller les comportements anormaux ou les pics de téléchargement de paquets peu connus dans leurs dépôts.

---
[Source](https://thehackernews.com/2025/10/10-npm-packages-caught-stealing.html){:target="_blank"}
