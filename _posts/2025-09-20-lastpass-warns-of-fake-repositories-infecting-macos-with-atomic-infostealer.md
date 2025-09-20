---
title: 'LastPass Warns of Fake Repositories Infecting macOS with Atomic Infostealer'
date: 2025-09-20
permalink: /posts/2025/09/20/lastpass-warns-of-fake-repositories-infecting-macos-with-atomic-infostealer/
tags:
- veille-cyber
- hackernews
---
**Faux Dépôts GitHub : Une Menace pour les Utilisateurs macOS**

Une campagne de malware sophistiquée cible les utilisateurs de macOS en exploitant de faux dépôts GitHub. Ces dépôts malveillants redirigent les victimes vers des programmes infectés par le logiciel espion "Atomic Infostealer". L'objectif est de dérober des informations sensibles aux utilisateurs.

Plusieurs applications populaires sont imitées, notamment 1Password, LastPass, Dropbox, et Notion, parmi d'autres. Les attaquants utilisent le référencement (SEO) pour manipuler les résultats des moteurs de recherche (Bing et Google), plaçant les liens vers leurs sites GitHub frauduleux en tête des listes. Les fausses pages GitHub incitent les utilisateurs à télécharger des programmes sous de faux prétextes, comme "Installer LastPass sur MacBook".

Le processus implique une redirection vers un autre domaine où des instructions, similaires à celles de ClickFix, demandent aux utilisateurs de copier et d'exécuter une commande dans le Terminal. Cela conduit à l'installation du malware Atomic Stealer, conçu pour communiquer avec un serveur distant. Des tactiques similaires impliquant des publicités sponsorisées et des "dangling commits" sur GitHub ont déjà été observées pour distribuer des malwares sur macOS.

**Points Clés :**

*   **Vecteur d'attaque :** Faux dépôts GitHub imitant des outils légitimes.
*   **Malware :** Atomic Infostealer (également appelé Atomic Stealer).
*   **Cible :** Utilisateurs de macOS.
*   **Méthode de distribution :** SEO poisoning pour manipuler les résultats de recherche, fausses instructions sur des pages GitHub.
*   **Objectif du malware :** Vol d'informations sensibles.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. L'attaque repose sur la tromperie des utilisateurs et la confiance accordée aux dépôts GitHub.

**Recommandations :**

*   Être vigilant face aux résultats de recherche menant à des téléchargements de logiciels, même s'ils semblent légitimes.
*   Vérifier attentivement l'authenticité des dépôts GitHub avant de télécharger quoi que ce soit.
*   Privilégier les canaux de téléchargement officiels et reconnus pour les logiciels.
*   Rester informé des dernières menaces de cybersécurité.

---
[Source](https://thehackernews.com/2025/09/lastpass-warns-of-fake-repositories.html){:target="_blank"}
