---
title: 'Max severity SAP Commerce Cloud flaw now targeted in attacks'
date: 2026-08-14
permalink: /posts/2026/08/14/max-severity-sap-commerce-cloud-flaw-now-targeted-in-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation active de la faille critique dans SAP Commerce Cloud

Une vulnérabilité critique d'exécution de code à distance (RCE) dans SAP Commerce Cloud, corrigée le 12 août 2026, fait actuellement l'objet d'attaques actives. Des chercheurs en sécurité ont confirmé des tentatives d'exploitation seulement trois jours après la publication du correctif.

**Vulnérabilité identifiée :**
*   **CVE-2026-58231** : Une faille de sévérité maximale (score CVSS 10.0) située dans le composant *Data Hub Adapter*. Elle permet à un attaquant non authentifié d'exécuter du code arbitraire en exploitant un défaut d'autorisation et une validation insuffisante des entrées utilisateur.

**Points clés :**
*   **Impact :** Compromission totale de l'application (confidentialité, intégrité et disponibilité).
*   **Portée :** Plus de 4 200 instances de SAP Commerce Cloud sont exposées sur Internet, principalement en Europe et en Amérique du Nord.
*   **État de la menace :** Bien qu'aucun PoC (Proof of Concept) public ne soit connu, l'exploitation "dans la nature" est confirmée par des outils de détection (honeypots).

**Recommandations :**
*   **Mise à jour immédiate :** SAP exhorte tous ses clients et partenaires à appliquer sans délai le correctif publié dans la note de sécurité [SAP Note 3771065](https://me.sap.com/notes/3771065).
*   **Surveillance :** Les administrateurs doivent inspecter les journaux de leurs instances SAP Commerce Cloud à la recherche de tentatives d'accès non autorisées ou de comportements anormaux liés au *Data Hub Adapter*.

---
[Source](https://www.bleepingcomputer.com/news/security/max-severity-sap-commerce-cloud-flaw-now-targeted-in-attacks/){:target="_blank"}
