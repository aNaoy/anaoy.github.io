---
title: 'Malicious NPM packages fetch infostealer for Windows, Linux, macOS'
date: 2025-10-30
permalink: /posts/2025/10/30/malicious-npm-packages-fetch-infostealer-for-windows-linux-macos/
tags:
- veille-cyber
- bleepingcomp
---
**Malware déguisé dans des paquets NPM**

Dix paquets malveillants ont été découverts dans le registre npm, conçus pour ressembler à des projets légitimes. Ces paquets, qui ont été téléchargés près de 10 000 fois, déploient un composant de vol d'informations capable de cibler les systèmes Windows, Linux et macOS. Les paquets utilisent le typosquatting, exploitant les erreurs de frappe des noms de bibliothèques populaires telles que TypeScript, discord.js, ethers.js, nodemon, react-router-dom et zustand.

**Points clés :**

*   **Méthode d'attaque :** Typosquatting de noms de paquets populaires dans le registre npm.
*   **Fonctionnalité malveillante :** Téléchargement et exécution d'un composant de vol d'informations.
*   **Obfuscation :** Plusieurs couches d'obfuscation (wrapper eval auto-décryptant, XOR, payload encodé en URL, flux de contrôle) pour échapper à l'analyse statique.
*   **Tromperie :** Présentation d'un faux défi CAPTCHA en ASCII pour donner une fausse légitimité.
*   **Collecte de données :** Vol d'identifiants et de jetons sensibles à partir de gestionnaires de clés système, de navigateurs (Chromium, Firefox), de services d'authentification, de clés SSH et de jetons API (OAuth, JWT).
*   **Exfiltration :** Les données volées sont compressées et envoyées à un serveur de commande et de contrôle.

**Vulnérabilités (sans CVE spécifique mentionnée dans l'article) :**

*   Les paquets malveillants contournent les mécanismes d'analyse statique standard grâce à des techniques d'obfuscation.
*   Le script `postinstall` s'exécute automatiquement à l'installation, rendant la détection précoce difficile.

**Recommandations :**

*   Les développeurs ayant téléchargé l'un des paquets listés doivent nettoyer leur système et réinitialiser tous les jetons d'accès et mots de passe.
*   Vérifier attentivement les noms de paquets pour détecter les fautes de frappe lors du téléchargement depuis npm ou d'autres registres open source.
*   S'assurer que les paquets proviennent de sources fiables et de dépôts officiels.

**Paquets suspects identifiés :**

*   typescriptjs
*   deezcord.js
*   dizcordjs
*   dezcord.js
*   etherdjs
*   ethesjs
*   ethetsjs
*   nodemonjs
*   react-router-dom.js
*   zustand.js

---
[Source](https://www.bleepingcomputer.com/news/security/malicious-npm-packages-fetch-infostealer-for-windows-linux-macos/){:target="_blank"}
