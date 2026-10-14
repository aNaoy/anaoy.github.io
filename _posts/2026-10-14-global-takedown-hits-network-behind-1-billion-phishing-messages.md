---
title: 'Global takedown hits network behind 1 billion phishing messages'
date: 2026-10-14
permalink: /posts/2026/10/14/global-takedown-hits-network-behind-1-billion-phishing-messages/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement d'un réseau mondial de phishing massif

Une opération internationale menée par les autorités et Microsoft a neutralisé un écosystème cybercriminel majeur ayant diffusé plus d'un milliard de messages malveillants auprès de 75 000 organisations dans 150 pays. Ce réseau, centré autour du marché souterrain « YAM Store » (Storm-3119), fournissait des outils de phishing clés en main (kits CoGUI, Haozi, Iron Man).

**Points clés :**
* **Volume d'activité :** Plus de 750 millions de messages ciblant les utilisateurs Microsoft ont été envoyés depuis le début de l'année.
* **Méthodes d'usurpation :** Utilisation d'outils d'IA pour créer de fausses organisations crédibles et rachat de domaines expirés d'entreprises légitimes pour héberger des infrastructures frauduleuses.
* **Techniques d'attaque :** Les kits de phishing intégraient des fonctions de géorepérage, de filtrage IP et de faux CAPTCHA pour contourner les outils d'analyse de sécurité. Le « device-code phishing » était massivement utilisé pour voler des jetons d'authentification.
* **Infrastructure :** Abus des services SharePoint et OneDrive pour l'hébergement de contenus malveillants et utilisation d'identifiants d'applications compromis pour la gestion des comptes.

**Vulnérabilités exploitées :**
* Aucun CVE spécifique n'est mentionné, l'attaque reposant sur l'exploitation des processus métiers (Business Email Compromise) et le détournement de légitimité via des domaines expirés et des comptes Cloud compromis.
* Usage détourné des mécanismes d'authentification par code d'appareil (device-code phishing).

**Recommandations :**
* **Renforcement de l'authentification :** Privilégier les méthodes d'authentification MFA résistantes au phishing (clés FIDO2) plutôt que les codes d'appareil ou les SMS.
* **Surveillance des domaines :** Mettre en place une veille sur le cycle de vie des domaines corporatifs pour éviter le rachat par des tiers malveillants une fois expirés.
* **Gestion des accès :** Auditer régulièrement les autorisations accordées aux applications tierces dans les environnements cloud (Microsoft 365, Google) et révoquer les accès inutilisés ou suspects.
* **Éducation et filtrage :** Sensibiliser les utilisateurs aux techniques d'usurpation (fausses notifications de livraisons, amendes, etc.) et renforcer le filtrage des emails entrants par des solutions de sécurité avancées.

---
[Source](https://www.bleepingcomputer.com/news/security/global-takedown-hits-network-behind-1-billion-phishing-messages/){:target="_blank"}
