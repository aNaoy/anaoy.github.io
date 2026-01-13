---
title: 'Facebook login thieves now using browser-in-browser trick'
date: 2026-01-13
permalink: /posts/2026/01/13/facebook-login-thieves-now-using-browser-in-browser-trick/
tags:
- veille-cyber
- bleepingcomp
---
## L'astuce du faux navigateur pour voler des identifiants Facebook

Des cybercriminels utilisent de plus en plus une technique appelée "browser-in-the-browser" (BitB) pour dérober les identifiants de connexion des utilisateurs Facebook. Cette méthode, conçue par un chercheur en sécurité en 2022, simule une fenêtre de connexion d'authentification légitime à l'intérieur d'un navigateur web.

Les pirates ciblent Facebook en raison de sa large base d'utilisateurs pour lancer des escroqueries, collecter des données personnelles ou commettre des fraudes à l'identité. Les attaques récentes impliquent souvent des e-mails se faisant passer pour des avis d'infraction de droit d'auteur ou des notifications de sécurité de Meta, menaçant la suspension du compte ou signalant des connexions non autorisées. Ces e-mails contiennent des liens raccourcis et de fausses pages CAPTCHA pour renforcer la tromperie.

La technique BitB utilise un iframe pour créer une fausse fenêtre pop-up imitant l'interface de connexion de Facebook. Cette fenêtre peut être personnalisée avec un titre et une URL qui la rendent difficile à distinguer d'une authentique. Les attaquants exploitent également des plateformes d'hébergement cloud légitimes comme Netlify et Vercel pour héberger des pages de phishing qui imitent le portail du Centre de confidentialité de Meta, dirigeant les victimes vers de faux formulaires d'appel collectant des informations personnelles.

### Points clés

*   L'utilisation croissante de la technique "browser-in-the-browser" (BitB) pour le phishing ciblant Facebook.
*   Les pirates exploitent la familiarité des utilisateurs avec les flux d'authentification pour les tromper.
*   L'hébergement de pages de phishing sur des plateformes cloud légitimes et l'utilisation d'URL raccourcies pour contourner les filtres de sécurité.
*   L'objectif est de voler les identifiants de connexion Facebook pour diverses activités frauduleuses.

### Vulnérabilités

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article. La technique BitB exploite la psychologie de l'utilisateur et les limitations de la détection visuelle des fausses interfaces.

### Recommandations

*   **Ne jamais cliquer sur les liens intégrés dans les e-mails** pour des notifications de sécurité ou d'infraction. Naviguer manuellement vers l'URL officielle de Facebook dans un nouvel onglet.
*   Lors de l'apparition de fenêtres pop-up pour une connexion, **vérifier si la fenêtre peut être déplacée en dehors de la fenêtre principale du navigateur**. Les iframes utilisés dans la technique BitB sont liés à la fenêtre sous-jacente et ne peuvent pas être tirés à l'extérieur.
*   **Activer l'authentification à deux facteurs (2FA)** sur son compte Facebook pour ajouter une couche de sécurité supplémentaire, même si les identifiants sont compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/facebook-login-thieves-now-using-browser-in-browser-trick/){:target="_blank"}
