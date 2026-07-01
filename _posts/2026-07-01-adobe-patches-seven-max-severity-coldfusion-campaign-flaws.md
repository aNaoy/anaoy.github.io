---
title: 'Adobe patches seven max severity ColdFusion, Campaign flaws'
date: 2026-07-01
permalink: /posts/2026/07/01/adobe-patches-seven-max-severity-coldfusion-campaign-flaws/
tags:
- veille-cyber
- bleepingcomp
---
### Mises à jour critiques de sécurité chez Adobe : ColdFusion et Campaign

Adobe a publié des correctifs pour sept vulnérabilités de criticité maximale affectant les plateformes ColdFusion et Campaign Classic. Ces failles, classées en priorité 1, permettent des attaques peu complexes ne nécessitant aucune interaction utilisateur, avec un risque élevé d'exploitation. Parallèlement, Adobe a annoncé le passage à un rythme de publication bimensuel pour ses bulletins de sécurité à partir du 14 juillet 2026 afin d'accélérer la remédiation.

**Points clés :**
* **Risque élevé :** Bien qu'aucune exploitation active ne soit connue à ce jour, la nature critique des failles impose une vigilance immédiate.
* **Nouvelle stratégie :** Adobe adoptera désormais un calendrier de publication bimensuel (les 2e et 4e mardis du mois).
* **Cible :** Les vulnérabilités concernent principalement les déploiements sur site (on-premises).

**Vulnérabilités identifiées :**
* **ColdFusion (versions 2025.9, 2023.20 et antérieures) :** CVE-2026-48276, CVE-2026-48277, CVE-2026-48281, CVE-2026-48316, CVE-2026-48282. Ces failles permettent à un attaquant sans privilèges d'exécuter du code à distance (RCE).
* **Campaign Classic (version 7.4.3 build 9396 et antérieures) :** CVE-2026-48286. Risque d'exécution de code arbitraire dans le contexte de l'utilisateur.

**Recommandations :**
* **Application des correctifs :** Adobe recommande fortement aux administrateurs d'installer les mises à jour dans un délai maximal de 72 heures.
* **Environnements concernés :** Prioriser les instances sur site, les versions hébergées par Adobe ayant déjà été corrigées pour la faille Campaign.

---
[Source](https://www.bleepingcomputer.com/news/security/adobe-patches-seven-max-severity-coldfusion-campaign-flaws/){:target="_blank"}
