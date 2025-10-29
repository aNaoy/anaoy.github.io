---
title: 'Microsoft: DNS outage impacts Azure and Microsoft 365 services'
date: 2025-10-29
permalink: /posts/2025/10/29/microsoft-dns-outage-impacts-azure-and-microsoft-365-services/
tags:
- veille-cyber
- bleepingcomp
---
### Panne DNS mondiale affectant les services Microsoft

Une panne du système de noms de domaine (DNS) a perturbé de nombreux services Microsoft à l'échelle mondiale, empêchant les utilisateurs de se connecter aux réseaux d'entreprise et d'accéder à des plateformes comme Microsoft Azure et Microsoft 365. Les problèmes ont commencé vers 16h00 UTC, entraînant des difficultés d'accès au portail Azure, au centre d'administration Microsoft 365, à Intune, à Exchange, ainsi qu'à des services tels que Azure Front Door CDN. Des organisations telles que le système ferroviaire néerlandais ont également été touchées, impactant les plateformes de planification de voyage.

Les impacts incluent des échecs de requête intermittents, une latence et des problèmes d'authentification, empêchant les employés de se connecter à leurs plateformes professionnelles. Microsoft a initialement attribué ces problèmes à un dysfonctionnement DNS général, avant de préciser que la cause était un changement de configuration involontaire sur le service Azure Front Door.

**Points Clés :**

*   Panne DNS mondiale affectant les services Microsoft Azure et Microsoft 365.
*   Impact sur l'authentification, l'accès aux portails d'administration et à des services CDN.
*   La cause identifiée est un changement de configuration erroné sur Azure Front Door.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans cet article. L'incident est présenté comme une défaillance opérationnelle résultant d'une mauvaise configuration.

**Recommandations :**

*   Les clients rencontrant des problèmes d'accès au portail Azure ont été invités à utiliser des méthodes programmatiques (PowerShell, CLI) pour accéder à leurs ressources.
*   Microsoft a pris des mesures pour bloquer les modifications sur les services Azure Front Door et a initié un retour à un état fonctionnel antérieur.
*   La redirection du trafic affecté vers une infrastructure alternative a été mise en œuvre comme solution temporaire.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-dns-outage-impacts-azure-and-microsoft-365-services/){:target="_blank"}
