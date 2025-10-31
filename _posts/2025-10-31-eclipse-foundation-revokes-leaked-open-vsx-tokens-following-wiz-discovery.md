---
title: 'Eclipse Foundation Revokes Leaked Open VSX Tokens Following Wiz Discovery'
date: 2025-10-31
permalink: /posts/2025/10/31/eclipse-foundation-revokes-leaked-open-vsx-tokens-following-wiz-discovery/
tags:
- veille-cyber
- hackernews
---
**Sécurité du Marketplace des Extensions VS Code**

L'Eclipse Foundation a révoqué des jetons d'accès exposés sur le marketplace Open VSX, suite à leur découverte dans des dépôts publics. Ces jetons, issus d'erreurs de développeurs et non d'une faille de l'infrastructure Open VSX, auraient pu permettre à des acteurs malveillants de modifier ou publier des extensions, menaçant ainsi la chaîne d'approvisionnement logicielle.

**Points Clés :**

*   Des jetons d'accès pour des extensions VS Code ont été accidentellement divulgués dans des dépôts publics, affectant potentiellement les marketplaces de Microsoft VS Code et Open VSX.
*   L'Eclipse Foundation a pris des mesures pour révoquer les jetons compromis et a introduit un nouveau format de préfixe ("ovsxp_") pour les jetons afin de faciliter leur détection.
*   Des extensions associées à une campagne malveillante nommée "GlassWorm" ont été identifiées et supprimées. Il est précisé que ce malware n'était pas auto-réplicatif et nécessitait le vol d'identifiants de développeur pour se propager.

**Vulnérabilités :**

*   Les vulnérabilités identifiées découlent de la divulgation involontaire de jetons d'accès dans des dépôts publics. Les CVEs spécifiques ne sont pas mentionnés dans l'article.

**Recommandations :**

*   Réduction par défaut de la durée de vie des jetons afin de limiter l'impact des fuites accidentelles.
*   Facilitation de la révocation des jetons lors de la notification.
*   Mise en place d'un scan automatisé des extensions lors de leur publication pour détecter les codes malveillants ou les secrets intégrés.
*   La sécurité de la chaîne d'approvisionnement est une responsabilité partagée entre les éditeurs qui doivent gérer leurs jetons avec soin et les mainteneurs des marketplaces qui doivent améliorer leurs capacités de détection et de réponse.

---
[Source](https://thehackernews.com/2025/10/eclipse-foundation-revokes-leaked-open.html){:target="_blank"}
