---
title: 'Microsoft Patches 398 Flaws Including a Windows Driver Zero-Day Under Active Attack'
date: 2026-08-12
permalink: /posts/2026/08/12/microsoft-patches-398-flaws-including-a-windows-driver-zero-day-under-active-attack/
tags:
- veille-cyber
- hackernews
---
### Mise à jour de sécurité Microsoft : 398 vulnérabilités corrigées dont une faille zero-day active

Microsoft a publié son cycle de correctifs mensuel corrigeant 398 vulnérabilités, incluant 62 failles critiques. La priorité absolue est donnée à une vulnérabilité « zero-day » actuellement exploitée par le groupe Lazarus dans le cadre de campagnes d'attaques ciblées.

#### Points clés
*   **Zero-day active :** Une élévation de privilèges dans le noyau Windows est utilisée pour obtenir des droits SYSTEM à partir d'un accès initial.
*   **Risque majeur :** Quatre failles critiques (score CVSS 9.8) permettent l'exécution de code à distance (RCE) sans aucune interaction utilisateur ni authentification.
*   **SharePoint :** Finalisation du correctif pour une chaîne d'exploitation complexe initiée en juillet, permettant l'exécution de code à distance sur les serveurs sur site (on-premises).

#### Vulnérabilités majeures
*   **CVE-2026-68820 (Score 7.0) :** Faille « use-after-free » dans le pilote `afd.sys` (Windows). Utilisée activement pour élever les privilèges au niveau SYSTEM.
*   **CVE-2026-62878 (Score 9.8) :** Dépassement de tampon dans Windows DNS Server. Potentiellement "wormable" (propagation autonome).
*   **CVE-2026-62893 (Score 9.8) :** Faille RCE dans Windows Deployment Services via le protocole TFTP.
*   **CVE-2026-62815 (Score 9.8) :** Faille RCE dans l'implémentation du protocole QUIC.
*   **CVE-2026-59124 (Score 9.8) :** Faille RCE dans le composant HPC Pack.
*   **CVE-2026-63520 :** Volet « exécution de code » finalisant la chaîne d'attaque critique contre SharePoint.

#### Recommandations
1.  **Priorité absolue :** Appliquer immédiatement le correctif pour la **CVE-2026-68820** sur l'ensemble du parc Windows.
2.  **Gestion des serveurs exposés :** Prioriser le déploiement des correctifs pour DNS, WDS, QUIC et HPC Pack sur les services accessibles depuis le réseau.
3.  **SharePoint :** Vérifier que les serveurs SharePoint ont bien reçu le correctif d'authentification de juillet (**CVE-2026-55040**) ainsi que celui d'exécution de code d'août (**CVE-2026-63520**).
4.  **Inventaire :** Évaluer l'exposition des services critiques avant de prioriser les patchs restants.

---
[Source](https://thehackernews.com/2026/08/microsoft-patches-398-flaws-including.html){:target="_blank"}
