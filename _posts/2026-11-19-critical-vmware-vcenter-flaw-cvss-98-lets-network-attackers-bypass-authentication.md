---
title: 'Critical VMware vCenter Flaw (CVSS 9.8) Lets Network Attackers Bypass Authentication'
date: 2026-11-19
permalink: /posts/2026/11/19/critical-vmware-vcenter-flaw-cvss-98-lets-network-attackers-bypass-authentication/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans VMware vCenter : Contournement d'authentification

Une faille critique a été identifiée dans VMware vCenter, permettant à un attaquant disposant d'un accès réseau de contourner l'authentification et d'accéder au système sans autorisation.

**Points clés :**
*   **Vulnérabilité principale :** Un contournement d'authentification situé dans le service de répertoire VMware (VMware Directory Service).
*   **Impact :** Bien que Broadcom n'ait rapporté aucune exploitation active, le score CVSS de 9.8 témoigne d'un risque très élevé.
*   **Produits affectés :** VMware vCenter (versions 8.0, 9.0 et 9.1) et les solutions dérivées telles que VMware Cloud Foundation, vSphere Foundation et Telco Cloud Platform. Les versions antérieures (6.5, 6.7 et 7.0) sont également présumées vulnérables.
*   **Absence de contournement :** Broadcom précise qu'aucune solution de contournement (workaround) n'est disponible ; la mise à jour est indispensable.

**Vulnérabilités identifiées :**
*   **CVE-2026-123890 (Score 9.8) :** Contournement d'authentification critique.
*   **CVE-2026-123891 à CVE-2026-123894 :** Quatre vulnérabilités de sévérité modérée (6.7 à 8.1) concernant des injections SQL, des injections de commande, une élévation de privilèges vers root et un contournement de signature de jeton SAML.

**Recommandations :**
*   **Application immédiate des correctifs :** Broadcom classe cette intervention comme un changement d'urgence (méthodologie ITIL). Les administrateurs doivent prioriser l'installation des versions corrigées.
*   **Gestion des mises à jour :** Les correctifs sont cumulatifs. Il est impossible d'utiliser le système *Quick Patch* ; une mise à jour complète est requise.
*   **Vigilance sur les conflits :** Pour les utilisateurs de VMware Cloud Foundation, une attention particulière est nécessaire lors de la mise à jour pour éviter le problème "Back-in-Time" identifié avec la version 9.1.1. Il est conseillé de consulter l'avis de sécurité officiel pour valider la séquence d'installation.

---
[Source](https://thehackernews.com/2026/11/critical-vmware-vcenter-flaw-cvss-98.html){:target="_blank"}
