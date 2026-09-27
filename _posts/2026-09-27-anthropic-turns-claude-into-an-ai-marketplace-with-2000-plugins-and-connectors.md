---
title: 'Anthropic turns Claude into an AI marketplace with 2,000+ plugins and connectors'
date: 2026-09-27
permalink: /posts/2026/09/27/anthropic-turns-claude-into-an-ai-marketplace-with-2000-plugins-and-connectors/
tags:
- veille-cyber
- bleepingcomp
---
### Lancement de Claude Marketplace : Vers un écosystème d'IA ouvert

Anthropic a officiellement inauguré son « Claude Marketplace », une plateforme centralisée proposant plus de 2 000 plugins, connecteurs et agents IA. Ce portail permet aux entreprises (Atlassian, Google, Salesforce, CrowdStrike, etc.) d'intégrer directement leurs outils à Claude, tout en offrant aux organisations un accès à des services de conseil spécialisés pour le déploiement. Pour favoriser l'adoption, Anthropic permet à tout développeur de soumettre ses créations en utilisant le *Model Context Protocol* (MCP) et les *Agent Skills*.

**Points clés :**
* **Centralisation :** Regroupement de connecteurs, plugins et agents dans un format similaire à un magasin d'applications (type Play Store).
* **Partenariats stratégiques :** Implication de géants technologiques et de cabinets de conseil (Accenture, Deloitte) pour faciliter l'intégration en entreprise.
* **Ouverture :** Accès simplifié pour les développeurs tiers via le protocole MCP, visant à dépasser les limites des intégrations basiques.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée. Cependant, l'intégration massive de connecteurs tiers augmente la **surface d'attaque** de la plateforme. L'utilisation d'agents autonomes présente des risques inhérents liés aux autorisations d'accès aux données sensibles et à l'exécution de code ou d'actions au sein des systèmes tiers.

**Recommandations de sécurité :**
* **Gestion des permissions :** Appliquer strictement le principe du moindre privilège lors de l'activation d'agents ou de connecteurs accédant à des bases de données critiques.
* **Audit des intégrations :** Évaluer la fiabilité et les pratiques de sécurité des développeurs tiers avant toute mise en production.
* **Gouvernance des données :** S'assurer que les flux de données entre les outils tiers et Claude sont conformes aux politiques de confidentialité de l'organisation.
* **Surveillance active :** Surveiller les comportements anormaux des agents IA, particulièrement ceux disposant de droits d'écriture ou de modification sur les systèmes connectés.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/anthropic-turns-claude-into-an-ai-marketplace-with-2-000-plus-plugins-and-connectors/){:target="_blank"}
