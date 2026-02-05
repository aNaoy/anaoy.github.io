---
title: 'Microsoft to shut down Exchange Online EWS in April 2027'
date: 2026-02-05
permalink: /posts/2026/02/05/microsoft-to-shut-down-exchange-online-ews-in-april-2027/
tags:
- veille-cyber
- bleepingcomp
---
**Fin de l'API EWS d'Exchange Online : une transition vers Microsoft Graph**

Microsoft mettra fin au support de l'API Exchange Web Services (EWS) pour Exchange Online en avril 2027. Cette décision vise à aligner les services sur les exigences actuelles en matière de sécurité, d'échelle et de fiabilité. Le déploiement de cette transition débutera le 1er octobre 2026, avec un blocage progressif de l'API, bien que des listes blanches puissent temporairement maintenir l'accès. La désactivation finale sera effective en avril 2027, sans exception. L'API EWS continuera de fonctionner pour les installations Exchange Server locales.

**Points Clés :**

*   **Arrêt d'EWS pour Exchange Online :** L'API EWS cessera de fonctionner pour les environnements Exchange Online en avril 2027.
*   **Migration vers Microsoft Graph :** Les développeurs sont encouragés à migrer vers l'API Microsoft Graph, qui offre désormais une parité fonctionnelle quasi complète avec EWS.
*   **Impact sur les environnements hybrides :** Pour les scénarios hybrides, les applications accédant aux boîtes aux lettres cloud devront passer à Graph. L'utilisation de Exchange Server 2019 est requise pour que les boîtes aux lettres locales puissent communiquer avec Exchange Online via Graph.
*   **Calendrier de la transition :**
    *   Octobre 2026 : Blocage par défaut d'EWS pour Exchange Online.
    *   Avril 2027 : Arrêt définitif d'EWS pour Exchange Online.
*   **Communication de Microsoft :** Les administrateurs recevront des notifications mensuelles via le Centre de Messagerie, fournissant des rappels et des résumés d'utilisation spécifiques à leur organisation. Des tests de "scream tests" pourront être effectués pour identifier les dépendances cachées.

**Vulnérabilités :**

L'article ne mentionne pas de vulnérabilités spécifiques (avec CVE) directement liées à la fin de support d'EWS. La décision de Microsoft semble être motivée par des raisons de sécurité, d'échelle et de fiabilité obsolètes de l'API EWS, plutôt que par des failles de sécurité identifiées et exploitées.

**Recommandations :**

*   **Pour les développeurs :** Migrez dès que possible de l'API EWS vers l'API Microsoft Graph.
*   **Pour les administrateurs :**
    *   Identifiez et documentez toutes les applications et intégrations qui utilisent actuellement EWS pour accéder à Exchange Online.
    *   Planifiez la migration de ces applications vers l'API Microsoft Graph.
    *   Suivez les communications de Microsoft via le Centre de Messagerie pour rester informé des échéances et des étapes à suivre.
    *   Préparez votre environnement pour la transition, en particulier pour les scénarios hybrides.
    *   Utilisez les fonctionnalités de listes blanches avant le blocage par défaut, si une transition immédiate n'est pas possible, mais prévoyez une migration définitive.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-shut-down-exchange-web-services-in-cloud-in-2027/){:target="_blank"}
