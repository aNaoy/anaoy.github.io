---
title: 'Critical Juniper Networks PTX flaw allows full router takeover'
date: 2026-02-26
permalink: /posts/2026/02/26/critical-juniper-networks-ptx-flaw-allows-full-router-takeover/
tags:
- veille-cyber
- bleepingcomp
---
## Failles Critiques dans les Routeurs Juniper PTX

Une faille de sécurité majeure a été découverte dans le système d'exploitation Junos OS Evolved des routeurs PTX Series de Juniper Networks. Cette vulnérabilité permet à un attaquant non authentifié, déjà présent sur le réseau, d'exécuter du code à distance avec des privilèges root, aboutissant ainsi à une prise de contrôle complète du périphérique.

**Points Clés :**

*   La vulnérabilité concerne le framework "On-Box Anomaly Detection".
*   Le problème réside dans une mauvaise attribution de permissions qui permet un accès via un port externe au lieu de l'interface de routage interne prévue.
*   Le service affecté s'exécute par défaut avec des privilèges root.
*   Les routeurs PTX Series sont couramment utilisés par les fournisseurs d'accès à Internet, les opérateurs de télécommunications et les applications cloud.

**Vulnérabilités :**

*   **CVE-2026-21902 :** Incorrect permission assignment in the ‘On-Box Anomaly Detection’ framework.

**Versions Affectées :**

*   Junos OS Evolved avant les versions 25.4R1-S1-EVO et 25.4R2-EVO.
*   Les versions antérieures peuvent également être affectées si elles ne sont pas en fin de vie (EoL).
*   Les versions standard (non-Evolved) de Junos OS ne sont pas concernées par cette CVE spécifique.

**Recommandations :**

1.  **Mise à jour immédiate :** Installer les versions corrigées : 25.4R1-S1-EVO, 25.4R2-EVO, et 26.2R1-EVO.
2.  **Mesures temporaires (si la mise à jour n'est pas immédiate) :**
    *   Restreindre l'accès aux points d'extrémité vulnérables aux seuls réseaux de confiance via des filtres de pare-feu ou des listes de contrôle d'accès (ACL).
    *   Désactiver le service vulnérable à l'aide de la commande : `'request pfe anomalies disable'`

Juniper Networks n'était pas au courant d'exploitations malveillantes de cette faille au moment de la publication de l'avis de sécurité. Les équipements Juniper constituent une cible privilégiée pour les acteurs de menaces avancés en raison de leur utilisation dans des infrastructures critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-juniper-networks-ptx-flaw-allows-full-router-takeover/){:target="_blank"}
