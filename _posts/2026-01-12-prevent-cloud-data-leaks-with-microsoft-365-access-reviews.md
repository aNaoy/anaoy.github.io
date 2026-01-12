---
title: 'Prevent cloud data leaks with Microsoft 365 access reviews'
date: 2026-01-12
permalink: /posts/2026/01/12/prevent-cloud-data-leaks-with-microsoft-365-access-reviews/
tags:
- veille-cyber
- bleepingcomp
---
### Maîtriser le partage de données dans Microsoft 365

L'intégration transparente des fonctionnalités de partage dans des plateformes comme Microsoft 365, bien que pratique, peut rapidement engendrer une perte de contrôle sur les données de l'entreprise. Il est courant que les organisations manquent de visibilité sur ce que leurs utilisateurs partagent et avec qui, exposant ainsi des informations sensibles.

Ce phénomène, appelé "oversharing", se manifeste lorsque le contenu est partagé inutilement longtemps ou avec un nombre excessif de personnes. Cela peut provenir d'une négligence, comme l'oubli de révoquer l'accès d'un freelance après la fin d'un projet, ou de pratiques moins évidentes, telles que la conservation de documents dans des dossiers partagés avec d'anciens fournisseurs ou l'ajout de nouveaux membres à des canaux Teams sans révision des permissions existantes.

Les outils natifs de Microsoft 365 présentent des limitations significatives dans la gestion de ce risque. Les informations de partage sont dispersées entre SharePoint, Teams et OneDrive, sans aucune solution de reporting centralisée. Même des outils comme Entra ID Governance, bien qu'offrant des revues d'accès, se concentrent uniquement sur les comptes et les appartenances aux groupes, ignorant le partage de contenu lui-même. Cette absence de visibilité crée un angle mort majeur pour la sécurité, rendant les organisations vulnérables aux fuites accidentelles ou aux exfiltrations de données ciblées.

La solution proposée pour pallier ces lacunes réside dans l'implémentation de revues d'accès spécifiques au contenu partagé. Ces revues permettent d'obtenir une vue d'ensemble centralisée du partage de contenu sur les différentes plateformes M365. Elles incitent les utilisateurs et les propriétaires de canaux/sites à examiner les liens de partage et les permissions, facilitant ainsi la révocation des accès devenus obsolètes ou risqués. Un suivi d'audit complet des actions entreprises et des décisions prises par les réviseurs, ainsi que l'application automatisée des résultats de ces revues, contribuent à renforcer la gouvernance de l'accès au cloud et à prévenir les fuites de données.

**Points clés :**

*   La facilité de partage dans Microsoft 365 conduit à une perte de contrôle et à une exposition des données.
*   L'"oversharing" (partage excessif) représente un risque de sécurité majeur.
*   Les outils natifs de Microsoft 365 manquent de visibilité centralisée sur le contenu partagé.
*   Les revues d'accès ciblées sur le contenu partagé sont nécessaires pour maîtriser ce risque.

**Vulnérabilités :**

*   Accès aux données conservés indéfiniment par des parties externes (freelances, anciens fournisseurs).
*   Accès accordé à l'ensemble du contenu d'un canal Teams, y compris des documents sensibles.
*   Stockage de données supplémentaires dans des dossiers partagés sans vérification des permissions existantes.
*   Partage via des chaînes d'e-mails non contrôlées.
*   Comptes inactifs conservant l'accès à des documents cloud.

**Recommandations :**

*   Mettre en œuvre des revues d'accès régulières spécifiquement pour le contenu partagé.
*   Obtenir une vue d'ensemble centralisée du contenu partagé sur Teams, OneDrive et SharePoint.
*   Permettre aux utilisateurs et aux propriétaires de sites/canaux de réviser et de révoquer les partages.
*   Établir un suivi d'audit complet des décisions de revue.
*   Automatiser l'application des résultats des revues pour révoquer les accès non conformes.

---
[Source](https://www.bleepingcomputer.com/news/security/prevent-cloud-data-leaks-with-microsoft-365-access-reviews/){:target="_blank"}
