---
title: 'Starkiller Phishing Suite Uses AitM Reverse Proxy to Bypass Multi-Factor Authentication'
date: 2026-03-03
permalink: /posts/2026/03/03/starkiller-phishing-suite-uses-aitm-reverse-proxy-to-bypass-multi-factor-authentication/
tags:
- veille-cyber
- hackernews
---
### Starkiller : Une Nouvelle Menace de Phishing Sophistiqué Contourne l'Authentification Multifactorielle

Une nouvelle plateforme de phishing baptisée "Starkiller" permet à des cybercriminels de contourner l'authentification multifactorielle (MFA) en utilisant un système de proxy inverse. Cette solution, proposée comme un service aux attaquants, leur permet de se faire passer pour des marques légitimes en affichant des pages de connexion réelles via leur propre infrastructure.

Grâce à l'utilisation d'une instance headless de Chrome encapsulée dans un conteneur Docker, Starkiller agit comme un intermédiaire entre la victime et le site légitime. Le contenu de la page d'origine est ainsi servi directement, assurant que les pages de phishing restent toujours à jour et évitant la création de modèles statiques identifiables par les outils de sécurité. Tous les éléments saisis par l'utilisateur, y compris les identifiants et les jetons de session, sont interceptés avant d'atteindre le site cible. L'ensemble du processus est géré via un tableau de bord centralisé, facilitant l'orchestration des campagnes de phishing, même pour des acteurs peu expérimentés.

Ce développement s'inscrit dans une tendance accrue de solutions de phishing offrant des flux de travail similaires à des modèles SaaS, abaissant ainsi le seuil de compétence requis pour mener des attaques à grande échelle. D'autres kits comme "1Phish" évoluent également pour inclure des fonctionnalités avancées, telles que la capture de codes à usage unique et le contournement de l'authentification via l'exploitation du flux d'autorisation de périphérique OAuth 2.0 pour compromettre les comptes Microsoft 365. Des campagnes ciblant le secteur financier démontrent également des tactiques sophistiquées, incluant l'utilisation de domaines frauduleux imitant des institutions financières et des pages d'attente trompeuses pour dissimuler le vol d'identifiants.

**Points Clés :**

*   **Plateforme Starkiller :** Un service de phishing qui utilise un proxy inverse pour contourner la MFA.
*   **Technologie :** Utilise un conteneur Docker et une instance Chrome headless pour afficher des pages de connexion réelles.
*   **Fonctionnalités :** Permet de choisir des marques à imiter, intègre des raccourcisseurs d'URL, et centralise la gestion des campagnes.
*   **Objectif :** Voler des identifiants et des jetons de session pour permettre la prise de contrôle de comptes.
*   **Tendances :** Évolution des kits de phishing vers des modèles SaaS et utilisation de techniques avancées comme l'exploitation d'OAuth 2.0 pour contourner la MFA.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est explicitement mentionnée pour Starkiller dans cet article. La menace réside dans l'exploitation de techniques de phishing et de contournement des mécanismes de sécurité existants.

**Recommandations :**

*   **Vigilance accrue :** Être très prudent face aux e-mails de phishing, même s'ils semblent provenir de sources légitimes.
*   **Vérification des URL :** Examiner attentivement les adresses URL avant de cliquer ou de saisir des informations sensibles.
*   **Authentification forte :** Utiliser et configurer correctement la MFA sur tous les comptes et les systèmes.
*   **Formation à la sécurité :** Sensibiliser les utilisateurs aux risques du phishing et aux techniques d'ingénierie sociale.
*   **Solutions de sécurité :** Mettre en œuvre des solutions de sécurité robustes, y compris des filtres anti-spam et anti-phishing, et maintenir les systèmes à jour.

---
[Source](https://thehackernews.com/2026/03/starkiller-phishing-suite-uses-aitm.html){:target="_blank"}
