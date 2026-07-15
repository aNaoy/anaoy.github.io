---
title: 'Firefox, Chrome, Adobe, and VMware Updates Fix Multiple Critical Security Flaws'
date: 2026-07-15
permalink: /posts/2026/07/15/firefox-chrome-adobe-and-vmware-updates-fix-multiple-critical-security-flaws/
tags:
- veille-cyber
- hackernews
---
### Vague de correctifs critiques pour Firefox, Chrome, Adobe et VMware

Plusieurs éditeurs majeurs ont publié des mises à jour urgentes pour corriger des failles de sécurité critiques dans leurs logiciels. Bien qu'aucune exploitation active ne soit actuellement recensée, la disponibilité publique de certains codes d'exploitation impose une mise à jour immédiate.

**Points clés :**
*   **Mozilla Firefox :** Correction de deux failles critiques (JavaScript/WebAssembly et isolation de site). Le code d'exploitation est déjà public.
*   **Google Chrome :** 15 vulnérabilités corrigées, dont deux failles critiques de type *Use-after-free* dans le composant Ozone.
*   **Adobe :** Déploiement massif de correctifs pour 88 vulnérabilités affectant ColdFusion, Commerce, Experience Manager et Illustrator.
*   **VMware :** Correction d'une faille critique de contournement d'authentification dans l'Avi Load Balancer.

**Vulnérabilités majeures identifiées :**
*   **Firefox :** CVE-2026-15718, CVE-2026-15719.
*   **Chrome :** CVE-2026-15764, CVE-2026-15765.
*   **Adobe ColdFusion :** CVE-2026-48318 (Score 9.9), CVE-2026-48322, CVE-2026-48284, CVE-2026-48321, CVE-2026-48325, CVE-2026-48319, CVE-2026-48324, CVE-2026-48327.
*   **Adobe Commerce/Magento :** CVE-2026-48356, CVE-2026-48358.
*   **Adobe Experience Manager :** CVE-2026-48259, CVE-2026-48359.
*   **VMware Avi Load Balancer :** CVE-2026-47865 (Score 9.8).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs vers les versions les plus récentes proposées par les éditeurs (notamment Firefox 152.0.6 et Chrome version 150.0.7871.124 ou ultérieure).
*   **Priorisation :** Accorder une priorité absolue aux serveurs et infrastructures exposés (Adobe ColdFusion et VMware Avi Load Balancer) en raison de la sévérité des scores CVSS.
*   **Veille :** Surveiller les bulletins de sécurité officiels pour s'assurer qu'aucune autre composante de l'environnement n'est impactée par les correctifs Adobe.

---
[Source](https://thehackernews.com/2026/07/firefox-chrome-adobe-and-vmware-updates.html){:target="_blank"}
