---
title: 'Mirage2FA Surge Hits 4,500 US and EU Companies, Abusing Microsoft 365 Login Flows'
date: 2026-08-25
permalink: /posts/2026/08/25/mirage2fa-surge-hits-4500-us-and-eu-companies-abusing-microsoft-365-login-flows/
tags:
- veille-cyber
- hackernews
---
### Menace Mirage2FA : Détournement de sessions Microsoft 365 à grande échelle

La campagne Mirage2FA est un service de phishing sophistiqué ayant ciblé plus de 4 500 entreprises entre 2024 et 2026, principalement aux États-Unis. Ce kit exploite des flux de connexion légitimes à Microsoft 365 pour dérober des jetons de session, permettant ainsi de contourner les mécanismes d'authentification à deux facteurs (2FA) traditionnels.

**Points clés :**
* **Ciblage :** Les secteurs de la technologie, de la fabrication et de l'éducation sont les plus touchés.
* **Mécanisme :** Attaque de type *AiTM (Adversary-in-the-Middle)* capturant les mots de passe et les cookies de session pour usurper l'identité des utilisateurs.
* **Conséquences :** Accès non autorisé aux emails, aux applications connectées via SSO et aux données sensibles, rendant la compromission difficile à détecter par de simples changements de mots de passe.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, car il s'agit d'une exploitation de la logique des flux d'authentification (phishing et vol de session) plutôt que d'une faille logicielle isolée. Le risque repose sur la vulnérabilité intrinsèque des méthodes 2FA classiques face aux attaques par interception de session.

**Recommandations :**
* **Renforcer l'authentification :** Migrer vers des méthodes d'authentification résistantes au phishing (ex: clés FIDO2/WebAuthn).
* **Détection comportementale :** Utiliser des solutions de "bac à sable" (sandbox) interactives pour isoler et analyser les URLs et pièces jointes suspectes en temps réel.
* **Gestion des incidents :** Traiter le vol de session comme un incident d'identité majeur. En cas de suspicion, il est impératif de révoquer immédiatement les sessions et jetons actifs, au lieu de se limiter à une réinitialisation de mot de passe.
* **Intelligence sur les menaces :** Surveiller les indicateurs d'infrastructure (scripts suspects, activité WebSocket, domaines récurrents) plutôt que de se fier uniquement aux IOC individuels.

---
[Source](https://thehackernews.com/2026/08/mirage2fa-surge-hits-4500-us-and-eu.html){:target="_blank"}
