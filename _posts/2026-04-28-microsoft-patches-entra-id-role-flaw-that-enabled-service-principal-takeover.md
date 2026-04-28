---
title: 'Microsoft Patches Entra ID Role Flaw That Enabled Service Principal Takeover'
date: 2026-04-28
permalink: /posts/2026/04/28/microsoft-patches-entra-id-role-flaw-that-enabled-service-principal-takeover/
tags:
- veille-cyber
- hackernews
---
### Escalade de privilèges via le rôle « Agent ID Administrator » dans Microsoft Entra ID

Une vulnérabilité majeure au sein de Microsoft Entra ID permettait une élévation de privilèges via le rôle administratif *Agent ID Administrator*. Initialement conçu pour gérer le cycle de vie des agents d'intelligence artificielle, ce rôle présentait un défaut de portée (scope overreach) permettant à ses détenteurs de s'approprier n'importe quel *service principal* au sein d'un locataire (tenant), et non uniquement ceux liés aux agents.

**Points clés :**
* **Vecteur d'attaque :** En devenant propriétaire d'un *service principal* arbitraire, un attaquant pouvait ajouter ses propres identifiants (clés, secrets) pour usurper l'identité du service.
* **Impact :** Si le *service principal* compromis possédait des rôles à hauts privilèges dans l'annuaire ou des autorisations Graph étendues, l'attaquant pouvait obtenir un contrôle total sur l'environnement cloud.
* **Vulnérabilité :** Il n'y a pas de CVE spécifique assignée à ce problème d'architecture, mais Microsoft a corrigé le défaut le 9 avril 2026 suite à un signalement responsable.

**Recommandations :**
* **Surveillance active :** Auditer régulièrement les changements de propriété des *service principals* et la création de nouveaux identifiants (secrets/certificats) associés.
* **Gestion des privilèges :** Restreindre strictement l'attribution du rôle *Agent ID Administrator* et surveiller l'usage des rôles à haut privilège.
* **Sécurisation :** Appliquer le principe du moindre privilège aux *service principals* et auditer périodiquement leur posture de sécurité pour limiter l'impact d'une compromission potentielle.
* **Validation :** S'assurer que les rôles administratifs disposent d'un périmètre d'action limité aux ressources strictement nécessaires, conformément à la logique de segmentation des identités.

---
[Source](https://thehackernews.com/2026/04/microsoft-patches-entra-id-role-flaw.html){:target="_blank"}
