---
title: 'Tycoon2FA phishing platform returns after recent police disruption'
date: 2026-03-24
permalink: /posts/2026/03/24/tycoon2fa-phishing-platform-returns-after-recent-police-disruption/
tags:
- veille-cyber
- bleepingcomp
---
### Résurgence rapide de la plateforme de phishing Tycoon2FA

La plateforme de phishing-as-a-service (PhaaS) Tycoon2FA est redevenue pleinement opérationnelle seulement quelques jours après son démantèlement par Europol et Microsoft, le 4 mars dernier. Malgré la saisie de 330 domaines, les cybercriminels ont rapidement restauré leur infrastructure, confirmant la résilience de ce service qui génère environ 30 millions d'e-mails malveillants par mois.

**Points clés :**
* **Nature de la menace :** Plateforme spécialisée dans le détournement de comptes Microsoft 365 et Gmail.
* **Méthodes d'attaque :** Utilisation de techniques *Adversary-in-the-Middle* (AitM) pour contourner l'authentification à deux facteurs (2FA).
* **Impact :** La plateforme représente 62 % des e-mails bloqués par Microsoft.
* **Activités post-compromission :** Création de règles de messagerie, dossiers cachés et préparation d'attaques BEC (*Business Email Compromise*), détournement de fils de discussion et exploitation de liens SharePoint malveillants.
* **Infrastructure :** Utilisation de services de raccourcissement d'URL, de plateformes légitimes détournées et de domaines compromis pour héberger les pages de phishing.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, car Tycoon2FA repose sur l'ingénierie sociale et des techniques de contournement de session (AitM) plutôt que sur l'exploitation de failles logicielles documentées.

**Recommandations :**
* **Sensibilisation :** Former les utilisateurs à repérer les e-mails suspects, même lorsqu'ils proviennent de plateformes ou d'outils légitimes.
* **Authentification renforcée :** Privilégier les clés de sécurité matérielles (FIDO2/WebAuthn) qui sont résistantes aux attaques de phishing de type AitM, contrairement aux codes SMS ou aux applications d'authentification classiques.
* **Surveillance proactive :** Analyser régulièrement les règles de transfert automatique et de création de dossiers au sein des messageries d'entreprise pour détecter toute activité inhabituelle typique d'une compromission (BEC).
* **Hygiène numérique :** Mettre en œuvre des solutions de filtrage d'e-mails avancées capables de détecter les pages de phishing générées par IA et les redirections malveillantes.

---
[Source](https://www.bleepingcomputer.com/news/security/tycoon2fa-phishing-platform-returns-after-recent-police-disruption/){:target="_blank"}
