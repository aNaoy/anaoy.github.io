---
title: 'AI website builder Lovable increasingly abused for malicious activity'
date: 2025-08-21
permalink: /posts/2025/08/21/ai-website-builder-lovable-increasingly-abused-for-malicious-activity/
tags:
- veille-cyber
- bleepingcomp
---
**Lovable : Une plateforme de création de sites web détournée pour des activités malveillantes**

La plateforme de création et d'hébergement de sites web assistée par intelligence artificielle, Lovable, est de plus en plus utilisée par les cybercriminels pour créer des pages de phishing, des portails de distribution de logiciels malveillants et divers sites frauduleux. Ces sites usurpent l'identité de grandes marques reconnues et intègrent des systèmes de filtrage comme les CAPTCHA pour repousser les robots.

Depuis février, des dizaines de milliers d'URL hébergées sur Lovable ont été détectées comme menaces dans des courriels. Des campagnes notables incluent :

*   Une opération à grande échelle utilisant la plateforme "phishing-as-a-service" Tycoon, qui redirigeait les utilisateurs vers de fausses pages de connexion Microsoft (avec authentification Azure AD ou Okta) pour voler des identifiants, des jetons MFA et des cookies de session.
*   Une campagne de vol de paiement et de données ciblant UPS, qui demandait aux victimes des informations personnelles, des numéros de carte de crédit et des codes SMS via de fausses pages.
*   Une campagne de vol de cryptomonnaies usurpant l'identité de la plateforme DeFi Aave, incitant les utilisateurs à connecter leurs portefeuilles à des pages frauduleuses.
*   Une campagne de distribution de logiciels malveillants, notamment le RAT zgRAT, en utilisant de fausses pages de portail de facturation distribuant des archives contenant des DLL infectées.

Bien que Lovable ait mis en place des mesures de détection en temps réel et des scans quotidiens pour identifier et supprimer les tentatives de fraude, des tests récents montrent que la plateforme peut encore être utilisée pour créer des sites malveillants sans opposition. Lovable a déclaré avoir implémenté un programme de sécurité basé sur l'IA pour bloquer les projets violant ses politiques et avoir supprimé plus de 300 sites frauduleux au cours des deux dernières semaines. La plateforme bloque environ 1000 projets uniques violant ses règles et affirme ne tolérer aucun contenu illégal ou malveillant.

**Points clés :**

*   Détournement de la plateforme Lovable par des cybercriminels.
*   Création de pages de phishing, de portails de malwares et de sites frauduleux.
*   Imitation de marques connues et utilisation de CAPTCHA.
*   Exemples de campagnes : vol d'identifiants Microsoft, vol de données UPS, vol de cryptomonnaies Aave, distribution de RAT zgRAT.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifiques directement liées à la plateforme Lovable, mais les sites malveillants créés exploitaient des techniques comme l'hameçonnage, l'usurpation d'identité, le vol d'authentification multifacteur (MFA) et la distribution de malwares (RAT, DOILoader).

**Recommandations :**

*   **Pour les utilisateurs :** Être vigilant face aux courriels suspects et aux liens, vérifier l'authenticité des sites web avant de saisir des informations personnelles ou financières.
*   **Pour les entreprises :** Renforcer la sensibilisation à la cybersécurité des employés, surveiller les tentatives de phishing et de fraude ciblant les marques.
*   **Pour les plateformes comme Lovable :** Continuer à améliorer les mesures de sécurité et de détection proactive pour prévenir l'abus par des acteurs malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/ai-website-builder-lovable-increasingly-abused-for-malicious-activity/){:target="_blank"}
