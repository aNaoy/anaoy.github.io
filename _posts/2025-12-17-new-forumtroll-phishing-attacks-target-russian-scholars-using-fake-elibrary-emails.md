---
title: 'New ForumTroll Phishing Attacks Target Russian Scholars Using Fake eLibrary Emails'
date: 2025-12-17
permalink: /posts/2025/12/17/new-forumtroll-phishing-attacks-target-russian-scholars-using-fake-elibrary-emails/
tags:
- veille-cyber
- hackernews
---
## Nouvelle vague d'attaques ForumTroll : des universitaires russes ciblés via de faux e-mails eLibrary

Une campagne de phishing sophistiquée, attribuée à un acteur de menace lié à "Operation ForumTroll", cible des universitaires russes spécialisés en sciences politiques, relations internationales et économie mondiale. Les attaques, détectées en octobre 2025, succèdent à des campagnes antérieures visant des organisations.

Les emails frauduleux se font passer pour des communications de la bibliothèque électronique scientifique russe "eLibrary", envoyés depuis l'adresse "support@e-library[.]wiki". Le domaine, enregistré six mois avant le début de la campagne, a été exploité en hébergeant une copie du site légitime d'eLibrary pour gagner en crédibilité. Les messages incitent les victimes à télécharger un "rapport de plagiat" via un lien unique, qui déclenche le téléchargement d'une archive ZIP personnalisée avec les noms de la victime.

Cette archive contient un raccourci Windows qui, une fois exécuté, lance un script PowerShell. Ce dernier télécharge un payload depuis un serveur distant qui récupère une DLL finale pour établir un accès à distance. La victime reçoit alors un faux document PDF, tandis que l'attaquant prend le contrôle de son appareil via le framework de commande et contrôle (C2) "Tuoni".

"Operation ForumTroll" sévit en Russie et en Biélorussie depuis au moins 2022. Les experts suggèrent que ce groupe continuera de cibler des entités et des individus d'intérêt dans ces régions.

**Points Clés :**

*   **Cible :** Universitaires russes dans les domaines des sciences politiques, des relations internationales et de l'économie mondiale.
*   **Méthode :** Phishing par email se faisant passer pour la plateforme eLibrary.
*   **Appât :** Faux "rapport de plagiat" nécessitant un téléchargement.
*   **Charge Utile :** Téléchargement d'une archive ZIP, exécution d'un script PowerShell, installation du framework C2 "Tuoni" pour un accès à distance.
*   **Durée d'Opération :** Le groupe est actif depuis au moins 2022.

**Vulnérabilités :**

*   Dans le passé, "Operation ForumTroll" a exploité une vulnérabilité zero-day dans Google Chrome (CVE-2025-2783) pour déployer les backdoors "LeetAgent" et "Dante". L'article ne précise pas si de nouvelles vulnérabilités zero-day sont exploitées dans la campagne actuelle, mais mentionne l'utilisation de techniques d'ingénierie sociale et de domaines frauduleux.

**Recommandations :**

*   Faire preuve de la plus grande prudence face aux emails semblant provenir d'institutions académiques ou de bibliothèques, surtout s'ils contiennent des liens de téléchargement.
*   Vérifier l'authenticité de l'expéditeur et de l'adresse email.
*   Ne pas cliquer sur les liens suspects ni télécharger de pièces jointes inattendues.
*   S'assurer que les logiciels (navigateurs, systèmes d'exploitation) sont à jour pour bénéficier des correctifs de sécurité.

---
[Source](https://thehackernews.com/2025/12/new-forumtroll-phishing-attacks-target.html){:target="_blank"}
