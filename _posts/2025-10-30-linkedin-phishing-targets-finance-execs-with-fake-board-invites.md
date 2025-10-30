---
title: 'LinkedIn phishing targets finance execs with fake board invites'
date: 2025-10-30
permalink: /posts/2025/10/30/linkedin-phishing-targets-finance-execs-with-fake-board-invites/
tags:
- veille-cyber
- bleepingcomp
---
**Campagne de Phishing sur LinkedIn : Ciblage des Cadres Financiers**

Des pirates informatiques utilisent LinkedIn pour cibler des cadres du secteur financier, leur envoyant des messages directs déguisés en invitations à rejoindre des conseils d'administration. L'objectif est de voler leurs identifiants Microsoft.

La campagne, identifiée par Push Security, commence par un message sur LinkedIn proposant de rejoindre le conseil d'administration d'un nouveau fonds d'investissement appelé "Common Wealth". Les messages incitent les destinataires à cliquer sur un lien pour en savoir plus.

Ce lien déclenche une série de redirections, passant par un site contrôlé par l'attaquant avant d'atterrir sur une fausse page de connexion hébergée sur firebasestorage.googleapis[.]com. Cette page se présente comme un portail "LinkedIn Cloud Share" et contient de faux documents relatifs au poste.

Pour accéder à ces documents, il est demandé de cliquer sur un bouton "View with Microsoft", qui redirige ensuite vers une page de connexion Microsoft frauduleuse. Cette page, après avoir passé un captcha Cloudflare Turnstile destiné à tromper les outils automatisés, est conçue pour capturer les identifiants et les cookies de session de l'utilisateur.

L'utilisation de captchas et de services comme Cloudflare Turnstile vise à empêcher l'analyse automatisée des pages malveillantes.

Les domaines malveillants observés incluent payrails-canaccord[.]icu, boardproposalmeet[.]com et sqexclusiveboarddirect[.]icu.

**Points Clés :**

*   Les attaques de phishing ne se limitent plus aux emails et se propagent sur des plateformes comme LinkedIn.
*   Environ 34% des tentatives de phishing suivies par Push Security proviennent de canaux non-email, une augmentation significative par rapport aux mois précédents.
*   Les pirates ciblent des professionnels en utilisant des opportunités professionnelles ou des invitations fictives.
*   Les fausses pages de connexion tentent de reproduire fidèlement les sites légitimes pour tromper les utilisateurs.

**Vulnérabilités :**

*   Absence de CVE spécifique mentionnée dans l'article pour cette campagne.

**Recommandations :**

*   Être vigilant face aux messages LinkedIn inattendus proposant des opportunités d'affaires ou des invitations à des conseils d'administration.
*   Éviter de cliquer sur des liens partagés dans des messages directs, surtout s'ils semblent suspects.
*   Vérifier systématiquement l'identité de l'expéditeur et la légitimité de l'offre avant de s'engager.
*   Se méfier des liens utilisant des domaines avec des extensions de premier niveau inhabituelles (.icu, .xyz, .top).

---
[Source](https://www.bleepingcomputer.com/news/security/linkedin-phishing-targets-finance-execs-with-fake-board-invites/){:target="_blank"}
