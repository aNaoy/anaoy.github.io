---
title: 'Researchers Report 84 Flaws in 4G and 5G Cores, Including a Session Hijacking Flaw'
date: 2026-07-31
permalink: /posts/2026/07/31/researchers-report-84-flaws-in-4g-and-5g-cores-including-a-session-hijacking-flaw/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les infrastructures 4G et 5G : La menace des erreurs de confiance implicite

Des chercheurs de l'Université technologique de Nanyang ont révélé l'existence d'une classe de vulnérabilités généralisées, baptisées « erreurs de confiance implicite » (iTrue), affectant les cœurs de réseau 4G (LTE) et 5G. Ces failles découlent d'une confiance aveugle entre les composants du réseau, exacerbée par la transition vers des architectures cloud-natives qui élargissent la surface d'attaque.

**Points clés :**
* **Découverte massive :** 84 vulnérabilités identifiées dans sept implémentations open-source de réseaux 4G/5G, dont Open5GS, OpenAirInterface, free5GC et SD-Core.
* **Méthodologie :** Utilisation d'un système multi-agents assisté par IA (iFinder) pour automatiser la détection des failles et générer des preuves de concept.
* **Impact :** Les attaquants peuvent mener des attaques par déni de service (DoS) ou détourner des sessions utilisateur (session hijacking) en injectant des messages malveillants (GTP-C ou PFCP) au sein du réseau.
* **Persistance :** Certaines vulnérabilités 5G sont héritées des systèmes 4G, illustrant une mauvaise adaptation des protocoles legacy aux environnements modernes.

**Vulnérabilités notables :**
* La vulnérabilité principale permettant le détournement de session a été confirmée sur des équipements commerciaux. 
* **CVE-2026-8233 :** Corrigée dans le produit XproUPF de Dotouch (score CVSS 4.6). 80 autres vulnérabilités ont également reçu un identifiant CVE.

**Recommandations :**
* **Renforcement de la validation :** Implémenter une vérification rigoureuse du format et de la sémantique de tous les messages entrants, ne jamais considérer un message provenant d'un pair interne comme intrinsèquement sûr.
* **Sécurisation des limites de réseau :** Appliquer une segmentation réseau stricte et un contrôle des frontières pour empêcher les messages de signalisation (GTP/PFCP) de transiter là où ils ne devraient pas.
* **Remédiation urgente :** Les opérateurs et les fournisseurs doivent auditer leurs déploiements pour s'assurer que les validations de ressources et les contrôles de priorité (notamment sur les PDR dans le protocole PFCP) sont correctement appliqués.

---
[Source](https://thehackernews.com/2026/07/researchers-report-84-flaws-in-4g-and.html){:target="_blank"}
