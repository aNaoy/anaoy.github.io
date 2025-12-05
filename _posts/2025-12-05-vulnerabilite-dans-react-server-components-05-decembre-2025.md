---
title: 'Vulnérabilité dans React Server Components (05 décembre 2025)'
date: 2025-12-05
permalink: /posts/2025/12/05/vulnerabilite-dans-react-server-components-05-decembre-2025/
tags:
- veille-cyber
- certfr
---
**Exécution de Code Arbitraire via React Server Components**

Une faille de sécurité critique, baptisée "React2Shell" et identifiée par les codes CVE-2025-55182 (pour React) et CVE-2025-66478 (initialement attribué par Next.js mais rejeté pour cause de doublon), affecte les React Server Components et potentiellement les React Server Functions. Elle permet à un attaquant non authentifié de réaliser une exécution de code arbitraire à distance.

Cette vulnérabilité peut toucher une application dès lors qu'elle supporte les React Server Components, même sans utiliser explicitement les React Server Functions. Des frameworks comme Next.js peuvent implémenter ces fonctions par défaut.

Les systèmes suivants sont particulièrement concernés :

*   Expo sans les versions correctives de `react-server-dom-webpack`.
*   Next.js versions 14.x canary, et versions 15.x et 16.0.x antérieures aux correctifs spécifiques.
*   React router avec le support de l'API RSC sans les derniers correctifs.
*   Les paquets `react-server-dom-webpack`, `react-server-dom-parcel`, et `react-server-dom-turbopack` dans leurs versions antérieures aux versions correctives.
*   Redwood SDK versions antérieures à 1.0.0-alpha.0.
*   Vitejs avec le greffon `plugin-rsc` sans les derniers correctifs.
*   Waku sans les versions correctives de `react-server-dom-webpack`.

Des preuves de concept publiques existent déjà, et une exploitation massive est anticipée. Bien que des mesures de mitigation puissent être mises en place sur certains pare-feux applicatifs web, elles ne remplacent pas la mise à jour des composants concernés.

Il est fortement recommandé de mettre à jour les composants affectés vers les versions correctives fournies par les éditeurs respectifs.

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2025-ALE-014/){:target="_blank"}
