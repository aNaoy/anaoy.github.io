---
title: '26,400 Valid Cloud and AI Credentials Found Exposed in Public Gitee Repositories'
date: 2026-10-29
permalink: /posts/2026/10/29/26400-valid-cloud-and-ai-credentials-found-exposed-in-public-gitee-repositories/
tags:
- veille-cyber
- hackernews
---
### Exposition massive de clés d'API sur Gitee : 26 400 identifiants compromis

Une étude menée sur 7,25 millions de dépôts publics de la plateforme Gitee a révélé l'existence de 26 400 identifiants valides et exposés, incluant des clés pour des services cloud (Alibaba Cloud) et des plateformes d'IA (DeepSeek, OpenAI, Zhipu). Ces secrets, parfois présents dans l'historique des commits depuis des années, permettent un accès non autorisé aux ressources des utilisateurs.

**Points clés :**
* **Volume de l'exposition :** 26 400 clés actives identifiées, dont près de la moitié datent de 2025.
* **Services les plus touchés :** Alibaba Cloud (9 473 clés), YouTube API (3 805), DeepSeek (3 170), Zhipu BigModel (1 489) et OpenAI (1 348).
* **Méthodologie :** L'analyse a été réalisée via deux outils distincts, *TruffleHog* et *Kingfisher*, soulignant la nécessité d'utiliser plusieurs scanners, car aucun outil ne détecte seul l'intégralité des vulnérabilités.
* **Persistance :** La suppression d'une clé dans le code ou l'historique ne suffit pas à la révoquer ; elle reste valide jusqu'à sa désactivation manuelle côté fournisseur.

**Vulnérabilités :**
* Exposition de secrets (clés d'API, jetons) dans le contrôle de version (Git).
* Risques associés : usurpation d'identité, surfacturation, perte de données et interruption de service.
* Absence de mesures de protection (rotation automatique, restriction des privilèges).

**Recommandations :**
* **Révoquer immédiatement :** Toute clé ayant été poussée sur un dépôt public doit être considérée comme compromise. Il faut la désactiver et générer de nouveaux identifiants auprès du fournisseur.
* **Assainir le cycle de développement :** Ne jamais intégrer de secrets dans le code source. Utiliser des coffres-forts de gestion de secrets (Vault, services natifs des clouds).
* **Restreindre les permissions :** Appliquer le principe du moindre privilège en configurant des restrictions API strictes sur les clés générées.
* **Auditer en continu :** Intégrer des outils de scan de secrets (tels que TruffleHog ou Kingfisher) dans les pipelines CI/CD pour bloquer tout commit contenant des identifiants avant qu'ils ne soient rendus publics.

---
[Source](https://thehackernews.com/2026/10/26400-valid-cloud-and-ai-credentials.html){:target="_blank"}
