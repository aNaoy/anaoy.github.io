---
title: 'D-Link warns of new RCE flaws in end-of-life DIR-878 routers'
date: 2025-11-20
permalink: /posts/2025/11/20/d-link-warns-of-new-rce-flaws-in-end-of-life-dir-878-routers/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilités critiques sur des routeurs D-Link obsolètes**

Des failles de sécurité critiques ont été découvertes sur les routeurs D-Link DIR-878, bien que ces appareils aient atteint leur fin de vie en 2021. Ces vulnérabilités, dont des exemples de code d'exploitation sont disponibles, permettent une exécution de commandes à distance non authentifiée. Bien que classées comme de gravité moyenne, elles pourraient être exploitées par des acteurs malveillants pour intégrer ces appareils dans des botnets.

**Points clés :**

*   Trois vulnérabilités d'exécution de commandes à distance affectent tous les modèles et révisions matérielles du routeur DIR-878.
*   Ces appareils sont toujours disponibles à la vente, neufs ou d'occasion, malgré leur fin de support.
*   D-Link ne publiera pas de mises à jour de sécurité pour ce modèle.

**Vulnérabilités identifiées :**

*   **CVE-2025-60672 :** Exécution de commandes à distance non authentifiée via des paramètres de configuration de DNS dynamique (NVRAM).
*   **CVE-2025-60673 :** Exécution de commandes à distance non authentifiée via des paramètres de DMZ et une valeur d'adresse IP non nettoyée injectée dans des commandes iptables.
*   **CVE-2025-60674 :** Dépassement de tampon dans la gestion du stockage USB en raison d'un champ "Numéro de série" trop long (nécessite un accès physique ou au niveau du périphérique USB).
*   **CVE-2025-60676 :** Exécution de commandes arbitraires via des champs non nettoyés dans le fichier `/tmp/new_qos.rule`.

**Recommandations :**

*   Remplacer immédiatement les routeurs D-Link DIR-878 par un produit activement supporté et mis à jour par le fabricant.

---
[Source](https://www.bleepingcomputer.com/news/security/d-link-warns-of-new-rce-flaws-in-end-of-life-dir-878-routers/){:target="_blank"}
