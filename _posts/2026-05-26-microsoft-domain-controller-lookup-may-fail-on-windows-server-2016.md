---
title: 'Microsoft: Domain Controller lookup may fail on Windows Server 2016'
date: 2026-05-26
permalink: /posts/2026/05/26/microsoft-domain-controller-lookup-may-fail-on-windows-server-2016/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement de la découverte des contrôleurs de domaine sur Windows Server 2016

L'installation de la mise à jour de sécurité de mai 2026 (KB5087537) provoque une erreur critique sur les serveurs Windows Server 2016 dont le nom d'hôte comporte exactement 15 caractères. Ce problème empêche la découverte des contrôleurs de domaine (DCLocator), entraînant des échecs dans les applications et les opérations administratives dépendantes de cette fonction, comme la gestion des espaces de noms DFS.

**Points clés :**
*   **Cause :** Un conflit logiciel introduit par la mise à jour KB5087537.
*   **Impact :** Échec des requêtes de découverte de contrôleur de domaine (retournant l'erreur `ERROR_INVALID_PARAMETER`).
*   **Cible :** Systèmes Windows Server 2016 avec un nom d'hôte de 15 caractères.
*   **État :** Microsoft a confirmé l'incident et mène une enquête ; aucun correctif n'est disponible à ce jour.

**Vulnérabilités :**
*   Aucun identifiant CVE n'est associé à ce bug fonctionnel.

**Recommandations :**
*   **Surveillance :** Identifier les serveurs Windows Server 2016 dans l'infrastructure ayant un nom d'hôte de 15 caractères.
*   **Attente :** Surveiller les bulletins de support de Microsoft pour la publication d'un correctif.
*   **Plan de contingence :** En cas d'impact critique sur la production, évaluer la possibilité de suspendre ou de déployer la mise à jour KB5087537 avec précaution sur les machines concernées après avoir testé l'impact sur un environnement hors production.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-domain-controller-lookup-may-fail-on-windows-server-2016/){:target="_blank"}
