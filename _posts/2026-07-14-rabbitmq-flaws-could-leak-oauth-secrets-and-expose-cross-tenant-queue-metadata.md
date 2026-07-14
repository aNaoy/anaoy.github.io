---
title: 'RabbitMQ Flaws Could Leak OAuth Secrets and Expose Cross-Tenant Queue Metadata'
date: 2026-07-14
permalink: /posts/2026/07/14/rabbitmq-flaws-could-leak-oauth-secrets-and-expose-cross-tenant-queue-metadata/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans RabbitMQ : Risques d'usurpation et de fuite de données

Des chercheurs en sécurité ont identifié deux failles majeures dans le service de messagerie RabbitMQ, affectant les versions 3.13.0 et ultérieures. Ces vulnérabilités permettent l'exfiltration de secrets OAuth, le contournement des frontières entre locataires (tenants) et, dans certains cas, une prise de contrôle totale du broker.

**Points clés :**
*   Les failles exposent les infrastructures de messagerie d'entreprise, particulièrement dans les environnements cloud ou multi-locataires où l'interface de gestion est accessible.
*   Aucune preuve d'exploitation active n'a été constatée avant la divulgation publique.
*   Des correctifs ont été publiés dans les versions 4.3.0, 4.2.6, 4.1.11, 4.0.20 et 3.13.15.

**Vulnérabilités identifiées :**
*   **CVE-2026-57219 (Score CVSS 8.7) :** Un point de terminaison HTTP obsolète (`GET /api/auth`) divulgue le secret client OAuth. Un attaquant non authentifié peut utiliser ce secret pour obtenir un jeton administrateur et prendre le contrôle total du broker.
*   **CVE-2026-57221 (Score CVSS 5.3) :** Un défaut d'autorisation permet à tout utilisateur authentifié d'énumérer les files d'attente, les échanges et d'accéder aux statistiques de consommation au sein d'un hôte virtuel, indépendamment de ses permissions réelles.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs vers les dernières versions disponibles.
*   **Rotation des secrets :** Renouveler les secrets clients OAuth si l'interface de gestion est accessible via Internet.
*   **Durcissement réseau :** Restreindre strictement l'accès au port 15672 (interface de gestion) via des règles de pare-feu pour le rendre inaccessible depuis des réseaux non fiables.
*   **Segmentation :** Maintenir une séparation stricte des locataires via des hôtes virtuels distincts.

---
[Source](https://thehackernews.com/2026/07/rabbitmq-flaws-could-leak-oauth-secrets.html){:target="_blank"}
