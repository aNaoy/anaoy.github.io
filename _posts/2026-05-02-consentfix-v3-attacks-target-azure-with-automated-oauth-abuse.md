---
title: 'ConsentFix v3 attacks target Azure with automated OAuth abuse'
date: 2026-05-02
permalink: /posts/2026/05/02/consentfix-v3-attacks-target-azure-with-automated-oauth-abuse/
tags:
- veille-cyber
- bleepingcomp
---
### Menace accrue : La campagne de phishing ConsentFix v3 contre Azure

La technique « ConsentFix v3 » représente une évolution industrialisée des attaques de type *OAuth phishing*. Elle exploite le processus d'autorisation OAuth2 pour détourner des comptes Microsoft, y compris ceux protégés par l'authentification multifacteur (MFA), en automatisant l'échange de codes d'autorisation contre des jetons d'accès.

**Points clés :**
* **Automatisation via Pipedream :** Contrairement aux versions précédentes, la v3 utilise des plateformes serverless comme Pipedream pour capturer les codes d'autorisation, les échanger instantanément contre des jetons de rafraîchissement (*refresh tokens*) et exfiltrer les données en temps réel.
* **Ingénierie sociale ciblée :** Les attaquants récoltent des données sur les employés pour personnaliser les emails de phishing, utilisant des fichiers PDF hébergés sur DocSend pour contourner les filtres anti-spam.
* **Exploitation des applications de confiance :** L'attaque détourne le mécanisme de confiance par défaut accordé aux applications "first-party" de Microsoft et aux identifiants partagés (FOCI), permettant aux attaquants d'accéder aux ressources (emails, fichiers) sans déclencher d'alertes de connexion suspectes classiques.
* **Post-exploitation :** Les jetons volés sont importés dans des outils comme « Specter Portal » pour naviguer dans l'environnement Microsoft compromis.

**Vulnérabilités :**
Il n'existe pas de CVE spécifique, car cette attaque repose sur un abus logique des flux OAuth et de la confiance accordée aux applications natives de l'écosystème Microsoft, et non sur une faille logicielle isolée.

**Recommandations :**
* **Liaison de jetons (*Token Binding*) :** Appliquer le *token binding* sur les appareils de confiance pour lier l'utilisation des jetons à des machines spécifiques.
* **Détection comportementale :** Mettre en place des règles de détection basées sur les anomalies comportementales au sein du tenant Azure (connexions inhabituelles, accès API suspects).
* **Restrictions d'authentification :** Restreindre les politiques d'authentification des applications et limiter les autorisations accordées aux applications tierces.
* **Sensibilisation :** Former les utilisateurs à la méfiance vis-à-vis des demandes leur intimant de copier-coller ou de faire glisser des URL de type `localhost` dans leur navigateur, une étape caractéristique du flux d'attaque ConsentFix.

---
[Source](https://www.bleepingcomputer.com/news/security/consentfix-v3-attacks-target-azure-with-automated-oauth-abuse/){:target="_blank"}
