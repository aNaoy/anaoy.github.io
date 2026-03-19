---
title: 'FBI seizes Handala data leak site after Stryker cyberattack'
date: 2026-03-19
permalink: /posts/2026/03/19/fbi-seizes-handala-data-leak-site-after-stryker-cyberattack/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement du groupe hacktiviste Handala par le FBI

Le FBI a saisi les domaines du groupe de hacktivistes « Handala », lié à l'Iran, en réponse à une cyberattaque dévastatrice contre le géant des technologies médicales Stryker. Le groupe avait réussi à compromettre un compte administrateur pour réinitialiser à distance environ 80 000 appareils via Microsoft Intune.

**Points clés :**
*   **Cible :** La société Stryker, dont 80 000 appareils (ordinateurs et mobiles) ont été réinitialisés aux paramètres d'usine.
*   **Mode opératoire :** Utilisation d'un compte administrateur compromis pour envoyer une commande de « wipe » (effacement) massive via le service de gestion d'appareils Microsoft Intune.
*   **Sanction :** Saisie par le FBI des domaines *handala-redwanted[.]to* et *handala-hack[.]to*, confirmant l'implication présumée du groupe dans des activités cybercriminelles coordonnées par un acteur étatique étranger.
*   **Réaction du groupe :** Handala a reconnu la saisie et travaille actuellement au déploiement d'une infrastructure plus résiliente.

**Vulnérabilités exploitées :**
*   Bien qu'aucune CVE spécifique ne soit citée, l'attaque repose sur une **exploitation par abus de privilèges légitimes** (compromission de compte administrateur global) pour détourner les fonctionnalités natives de gestion d'appareils (Microsoft Intune).

**Recommandations de sécurité :**
*   **Renforcer l'accès à Intune :** Appliquer des politiques d'accès conditionnel strictes et mettre en place une authentification multifacteur (MFA) robuste pour tous les comptes administrateurs.
*   **Sécurisation des domaines Windows :** Surveiller étroitement la création de nouveaux comptes administrateurs et auditer régulièrement les droits d'accès sur les outils de gestion de flotte.
*   **Application des guides officiels :** Suivre les recommandations publiées par Microsoft et la CISA visant spécifiquement le durcissement de la configuration des environnements Microsoft Intune pour prévenir les détournements de commandes de réinitialisation.

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-seizes-handala-data-leak-site-after-stryker-cyberattack/){:target="_blank"}
