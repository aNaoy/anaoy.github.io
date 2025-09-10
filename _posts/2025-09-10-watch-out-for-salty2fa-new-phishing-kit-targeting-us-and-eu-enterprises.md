---
title: 'Watch Out for Salty2FA: New Phishing Kit Targeting US and EU Enterprises'
date: 2025-09-10
permalink: /posts/2025/09/10/watch-out-for-salty2fa-new-phishing-kit-targeting-us-and-eu-enterprises/
tags:
- veille-cyber
- hackernews
---
## Salty2FA : une menace de phishing évoluée ciblant les entreprises

Une nouvelle plateforme de phishing-as-a-Service (PhaaS) nommée Salty2FA sévit actuellement, visant spécifiquement les entreprises aux États-Unis et en Europe. Ce kit de phishing se distingue par sa capacité à contourner divers mécanismes d'authentification à deux facteurs (2FA), y compris les méthodes par push, SMS et appels vocaux, rendant ainsi les informations d'identification volées directement exploitables pour une prise de contrôle de compte.

Les campagnes associées à Salty2FA ont débuté de manière significative en juin 2025, avec des traces remontant potentiellement à mars-avril. Les secteurs les plus touchés incluent la finance, l'énergie, les télécommunications, la santé, le gouvernement, la logistique, l'éducation et la construction aux États-Unis, ainsi que les télécommunications, la chimie, l'énergie (solaire), la fabrication industrielle, l'immobilier et le conseil en Europe (notamment au Royaume-Uni, en Allemagne, en Espagne, en Italie, en Grèce et en Suisse). Des activités mondiales sont également observées dans la logistique, l'informatique et la métallurgie.

Le fonctionnement typique de Salty2FA implique l'envoi d'e-mails de phishing trompeurs, utilisant des prétextes comme des "demandes de révision externe" ou des "corrections de paiement". Ces e-mails redirigent les victimes vers de fausses pages de connexion, souvent estampillées par des marques connues comme Microsoft et protégées par des filtres tels que Cloudflare pour masquer leur nature malveillante. Après avoir dérobé les identifiants, le système Salty2FA intercepte les codes 2FA nécessaires pour finaliser l'accès aux comptes.

**Points clés :**

*   **Nouveau kit de phishing-as-a-Service (PhaaS) :** Salty2FA est une menace émergente.
*   **Contournement de la 2FA :** Capable de subtiliser les codes des méthodes push, SMS et vocales.
*   **Ciblage géographique :** Principale activité observée aux États-Unis et en Europe.
*   **Secteurs visés :** Finance, énergie, télécommunications, santé, gouvernement, logistique, éducation, construction, chimie, fabrication industrielle, immobilier, conseil, informatique, métallurgie.
*   **Techniques d'ingénierie sociale :** Utilisation de leurres liés aux paiements et aux facturations.
*   **Infrastructure évolutive :** Utilisation de protections comme Cloudflare pour échapper à la détection.

**Vulnérabilités exploitées :**

Bien que l'article ne mentionne pas de CVE spécifiques liées à Salty2FA, la vulnérabilité fondamentale réside dans :

*   La **confiance des employés** dans les e-mails d'apparence légitime.
*   La **dépendance aux méthodes 2FA moins sécurisées** (SMS, appels vocaux).
*   La **difficulté de détecter des campagnes de phishing dynamiques** basées uniquement sur des indicateurs statiques.

**Recommandations :**

Pour contrer Salty2FA et des menaces similaires, les organisations sont encouragées à :

*   **Prioriser la détection comportementale :** Se concentrer sur les schémas d'attaque récurrents plutôt que sur des indicateurs statiques qui changent constamment.
*   **Utiliser des environnements de sandbox interactifs :** Analyser les e-mails suspects pour visualiser l'intégralité de la chaîne d'attaque en temps réel, y compris le vol d'identifiants et l'interception de 2FA.
*   **Renforcer les politiques MFA :** Privilégier les applications d'authentification ou les jetons matériels par rapport aux SMS et appels vocaux. Mettre en place un accès conditionnel pour les connexions à risque.
*   **Former les employés :** Sensibiliser aux leurres financiers courants, qui doivent toujours susciter la suspicion.
*   **Intégrer les résultats de sandbox :** Alimenter les systèmes SIEM/SOAR avec des données d'attaque en direct pour accélérer la détection et réduire la charge de travail manuelle des analystes.

---
[Source](https://thehackernews.com/2025/09/watch-out-for-salty2fa-new-phishing-kit.html){:target="_blank"}
