---
title: 'Microsoft releases emergency updates to fix Windows Server issues'
date: 2026-04-20
permalink: /posts/2026/04/20/microsoft-releases-emergency-updates-to-fix-windows-server-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Déploiement de correctifs d'urgence pour Windows Server

Microsoft a publié des mises à jour hors bande (OOB) pour corriger des dysfonctionnements critiques introduits par les correctifs de sécurité d'avril 2026 sur plusieurs versions de Windows Server.

**Points clés :**
*   **Échecs d'installation :** Certains serveurs rencontraient des erreurs lors de l'installation de la mise à jour KB5082063 sur Windows Server 2025.
*   **Boucles de redémarrage :** Les contrôleurs de domaine subissaient des redémarrages en boucle provoqués par le plantage du service LSASS (*Local Security Authority Subsystem Service*), notamment lors du traitement des demandes d'authentification au démarrage.
*   **Problème BitLocker :** Des serveurs sous Windows Server 2025 demandent désormais systématiquement une clé de récupération BitLocker après l'application des correctifs d'avril.

**Vulnérabilités :**
*   Aucun identifiant CVE spécifique n'est mentionné pour ces bogues fonctionnels, il s'agit de problèmes de stabilité et de comportement après mise à jour.

**Recommandations :**
*   Appliquer les correctifs d'urgence correspondants à votre version de système d'exploitation :
    *   **Windows Server 2025 :** KB5091157 (corrige à la fois l'échec d'installation et la boucle de redémarrage).
    *   **Versions 23H2, 2022, 2019, 2016 :** KB5091571, KB5091575, KB5091573, KB5091572 (traitent uniquement la boucle de redémarrage).
    *   **Azure Edition (Hotpatch) :** KB5091470 (2025) et KB5091576 (2022).
*   Prévoir une procédure de récupération des clés BitLocker pour les serveurs Windows Server 2025 impactés par le bug de démarrage.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-emergency-updates-to-fix-windows-server-issues/){:target="_blank"}
