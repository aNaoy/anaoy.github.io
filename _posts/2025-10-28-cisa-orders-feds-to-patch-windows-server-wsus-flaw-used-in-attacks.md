---
title: 'CISA orders feds to patch Windows Server WSUS flaw used in attacks'
date: 2025-10-28
permalink: /posts/2025/10/28/cisa-orders-feds-to-patch-windows-server-wsus-flaw-used-in-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Urgence de patch pour une faille WSUS critique**

La CISA a ordonné aux agences gouvernementales américaines de corriger une vulnérabilité critique affectant le service de mise à jour de Windows Server (WSUS). Cette faille, référencée sous le nom de **CVE-2025-59287**, est activement exploitée et potentiellement propagée de manière autonome. Elle permet à des attaquants, via des attaques de faible complexité ne nécessitant ni interaction utilisateur ni privilèges, d'obtenir des droits système et d'exécuter du code malveillant. Microsoft a publié des mises à jour d'urgence pour y remédier.

*   **Points clés :**
    *   La vulnérabilité affecte les serveurs Windows avec le rôle de serveur WSUS.
    *   Elle permet l'exécution de code à distance avec des privilèges système.
    *   Elle est activement exploitée dans la nature.
    *   La CISA l'a ajoutée à son catalogue des vulnérabilités connues exploitées.

*   **Vulnérabilité :**
    *   **CVE-2025-59287** (Windows Server Update Services Remote Code Execution Vulnerability)

*   **Recommandations :**
    *   Installer les mises à jour de sécurité d'urgence publiées par Microsoft dès que possible.
    *   Dans l'attente des correctifs, désactiver le rôle de serveur WSUS sur les systèmes vulnérables.
    *   Identifier tous les serveurs vulnérables et appliquer les mises à jour.
    *   Redémarrer les serveurs WSUS après l'installation des mises à jour pour une protection complète.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-orders-feds-to-patch-windows-server-wsus-flaw-exploited-in-attacks/){:target="_blank"}
