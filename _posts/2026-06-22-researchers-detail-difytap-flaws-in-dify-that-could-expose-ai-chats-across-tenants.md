---
title: 'Researchers Detail DifyTap Flaws in Dify That Could Expose AI Chats Across Tenants'
date: 2026-06-22
permalink: /posts/2026/06/22/researchers-detail-difytap-flaws-in-dify-that-could-expose-ai-chats-across-tenants/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques « DifyTap » dans la plateforme Dify

Des chercheurs en sécurité ont révélé l'existence de plusieurs failles critiques, regroupées sous le nom de **DifyTap**, affectant la plateforme d'agents IA open-source Dify. Ces vulnérabilités permettaient à des attaquants, parfois sans authentification, d'intercepter les échanges entre utilisateurs et modèles IA, d'accéder aux documents privés d'autres locataires (tenants) et d'exécuter des requêtes API internes non autorisées.

#### Points clés
* **Interception de données :** Les failles permettaient de rediriger les flux de messages vers des outils de traçage contrôlés par l'attaquant, créant un canal d'exfiltration furtif.
* **Accès inter-locataires :** Plusieurs vulnérabilités brisaient l'isolation logique entre les différents clients de la plateforme cloud, exposant des données confidentielles.
* **Défaillance de sécurité :** Le problème est en partie lié à une absence de vérification de propriété des ressources (tenant ownership) au sein des APIs internes et des services de fichiers.

#### Vulnérabilités identifiées
* **CVE-2024-5846 (Score 8.8) :** Utilisation d'une bibliothèque PDFium obsolète, permettant une corruption de mémoire (use-after-free).
* **CVE-2026-41947 (Score 9.1) :** Contournement d'autorisation permettant de modifier les configurations de traçage de n'importe quelle application.
* **CVE-2026-41948 (Score 9.4) :** Traversée de chemin (path traversal) dans l'API du Plugin Daemon permettant l'accès à des points de terminaison privés.
* **CVE-2026-41949 (Score 7.5) :** Contournement d'autorisation permettant de lire des extraits de documents d'autres locataires via leur UUID.
* **CVE-2026-41950 (Score 6.5) :** Accès non autorisé au contenu complet des fichiers d'autres utilisateurs au sein d'un même locataire.

#### Recommandations
* **Mise à jour :** Installer immédiatement la **version 1.14.2** de Dify, qui corrige la majorité des failles identifiées.
* **Suivi des correctifs :** Surveiller les prochaines publications de l'éditeur pour obtenir le correctif final concernant la vulnérabilité **CVE-2026-41948**, actuellement en attente de résolution.
* **Audit des conteneurs :** Les chercheurs soulignent que les outils de scan traditionnels peuvent manquer ces vulnérabilités au sein des images conteneurisées ; une vigilance accrue sur les dépendances et les configurations est nécessaire.

---
[Source](https://thehackernews.com/2026/06/researchers-detail-difytap-flaws-in.html){:target="_blank"}
