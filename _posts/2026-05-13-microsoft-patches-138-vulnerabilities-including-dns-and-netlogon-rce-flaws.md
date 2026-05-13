---
title: 'Microsoft Patches 138 Vulnerabilities, Including DNS and Netlogon RCE Flaws'
date: 2026-05-13
permalink: /posts/2026/05/13/microsoft-patches-138-vulnerabilities-including-dns-and-netlogon-rce-flaws/
tags:
- veille-cyber
- hackernews
---
### Mise à jour critique de sécurité Microsoft : 138 vulnérabilités corrigées

Microsoft a déployé des correctifs pour 138 vulnérabilités ce mois-ci, dont 30 classées comme critiques. Bien qu'aucune exploitation active ne soit signalée, l'augmentation du volume de failles détectées souligne l'impact croissant de l'IA (système MDASH) dans la découverte de vulnérabilités.

**Points clés :**
*   **Volume important :** 138 failles corrigées, incluant 61 vulnérabilités d'élévation de privilèges et 32 d'exécution de code à distance (RCE).
*   **Innovation IA :** Microsoft utilise désormais un système multi-modèle d'IA pour identifier proactivement les failles au sein de son infrastructure.
*   **Urgence "Secure Boot" :** Une mise à jour non-CVE est impérative avant le 26 juin 2026 pour renouveler les certificats Secure Boot, sous peine de pannes de démarrage majeures.

**Vulnérabilités majeures (Sélection) :**
*   **CVE-2026-41096 (Score 9.8) :** Dépassement de tampon dans Windows DNS permettant l'exécution de code à distance.
*   **CVE-2026-41089 (Score 9.8) :** Dépassement de tampon dans Windows Netlogon affectant les contrôleurs de domaine.
*   **CVE-2026-42826 (Score 10.0) :** Exposition d'informations sensibles dans Azure DevOps.
*   **CVE-2026-42898 / CVE-2026-33109 / CVE-2026-42823 (Score 9.9) :** Diverses failles critiques (injection de code, accès inapproprié) dans Dynamics 365, Azure Cassandra et Azure Logic Apps.
*   **CVE-2026-40402 (Score 9.3) :** Vulnérabilité *use-after-free* dans Hyper-V permettant une élévation de privilèges SYSTEM.
*   **CVE-2026-54518 (Score 7.3) :** Faille matérielle AMD (Zen 2) entraînant une possible élévation de privilèges.

**Recommandations :**
*   **Priorité absolue :** Appliquer la mise à jour des certificats *Secure Boot* avant l'échéance du 26 juin 2026.
*   **Gestion des correctifs :** Trier les vulnérabilités par niveau d'exposition et d'impact plutôt que par volume brut.
*   **Hygiène de sécurité :** Réduire l'exposition inutile à Internet, désactiver les méthodes d'authentification héritées (*legacy*), renforcer l'usage de l'authentification multifacteur (MFA) et segmenter les environnements réseau pour limiter les déplacements latéraux.
*   **Veille :** Maintenir une cadence de mise à jour rigoureuse pour s'adapter à la rapidité croissante de découverte des failles.

---
[Source](https://thehackernews.com/2026/05/microsoft-patches-138-vulnerabilities.html){:target="_blank"}
