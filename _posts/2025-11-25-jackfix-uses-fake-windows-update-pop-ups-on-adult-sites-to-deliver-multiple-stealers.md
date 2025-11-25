---
title: 'JackFix Uses Fake Windows Update Pop-Ups on Adult Sites to Deliver Multiple Stealers'
date: 2025-11-25
permalink: /posts/2025/11/25/jackfix-uses-fake-windows-update-pop-ups-on-adult-sites-to-deliver-multiple-stealers/
tags:
- veille-cyber
- hackernews
---
### Fraude par mise à jour Windows sur des sites pour adultes

Une nouvelle campagne de cyberattaques, nommée JackFix, utilise de faux pop-ups de mise à jour Windows sur des sites web pour adultes afin de diffuser des logiciels malveillants. Ces attaques exploitent la technique ClickFix, qui trompe les utilisateurs pour qu'ils exécutent des commandes malveillantes en se faisant passer pour des mises à jour de sécurité critiques.

**Points clés :**

*   La campagne cible les utilisateurs de sites pour adultes, qui sont plus susceptibles d'être sous pression psychologique pour installer des "mises à jour de sécurité" urgentes.
*   Les fausses alertes de mise à jour Windows prennent l'écran en otage et demandent à l'utilisateur d'ouvrir la boîte de dialogue "Exécuter", d'appuyer sur Ctrl+V et d'entrer pour déclencher l'infection.
*   La méthode d'infection initiale repose sur l'exécution d'un script JavaScript via MSHTA, qui télécharge ensuite un autre script PowerShell depuis un serveur distant.
*   Ces scripts sont obfusqués pour masquer le code malveillant et sont conçus pour ne répondre qu'à des commandes PowerShell spécifiques, rendant l'analyse plus difficile.
*   La campagne peut élever les privilèges de l'attaquant et désactiver des protections antivirus.
*   Elle déploie jusqu'à huit charges utiles différentes, incluant des "stealers" conçus pour voler des mots de passe, des portefeuilles de cryptomonnaies, et d'autres informations sensibles.

**Vulnérabilités :**

*   Bien qu'aucun numéro CVE spécifique ne soit mentionné, la vulnérabilité exploitée réside dans l'ingénierie sociale et la confiance accordée aux alertes de mise à jour système, combinées à la manipulation du navigateur et de l'exécution de scripts locaux. Les méthodes d'élévation de privilèges peuvent potentiellement exploiter des vulnérabilités système non spécifiées.

**Recommandations :**

*   Sensibiliser les employés à reconnaître les menaces d'ingénierie sociale et à se méfier des pop-ups inattendus, en particulier sur des sites web à risque.
*   Désactiver la boîte de dialogue "Exécuter" de Windows via des modifications du registre ou des stratégies de groupe (Group Policy).
*   Maintenir les systèmes d'exploitation et les logiciels antivirus à jour avec les derniers correctifs de sécurité.
*   Faire preuve de prudence extrême lors de l'interaction avec des éléments sur des sites web non fiables.

---
[Source](https://thehackernews.com/2025/11/jackfix-uses-fake-windows-update-pop.html){:target="_blank"}
