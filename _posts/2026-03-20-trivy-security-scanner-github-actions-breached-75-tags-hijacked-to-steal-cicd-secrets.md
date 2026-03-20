---
title: 'Trivy Security Scanner GitHub Actions Breached, 75 Tags Hijacked to Steal CI/CD Secrets'
date: 2026-03-20
permalink: /posts/2026/03/20/trivy-security-scanner-github-actions-breached-75-tags-hijacked-to-steal-cicd-secrets/
tags:
- veille-cyber
- hackernews
---
### Compromission de la Supply Chain : Attaque sur Trivy via les GitHub Actions

Trivy, l'outil d'analyse de vulnérabilités d'Aqua Security, a été victime d'une seconde compromission en moins d'un mois. Des attaquants ont exploité des identifiants compromis pour modifier 75 tags de version sur les dépôts `trivy-action` et `setup-trivy`. Cette manipulation a permis de rediriger les utilisateurs vers une version malveillante intégrant un infostealer, visant à exfiltrer des secrets CI/CD (clés SSH, tokens cloud, identifiants Kubernetes, portefeuilles crypto).

**Points clés :**
*   **Mode opératoire :** Utilisation de tags "force-pushés" pour distribuer un payload malveillant sans modifier les références de version standard.
*   **Menace :** Le malware (attribué potentiellement au groupe TeamPCP) scanne l'environnement à la recherche de variables d'environnement, chiffre les données et les exfiltre vers un serveur distant ou, en cas d'échec, via un dépôt public sur le compte GitHub de la victime.
*   **Cause racine :** Une rotation incomplète des secrets et tokens lors de l'incident précédent a permis aux attaquants de conserver un accès persistant.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, l'incident repose sur l'abus de privilèges d'accès légitimes (compromission de tokens/identifiants de mainteneurs) et la vulnérabilité intrinsèque à l'utilisation de tags de version dynamiques dans les pipelines CI/CD.

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions sécurisées : `trivy 0.69.3`, `trivy-action 0.35.0` et `setup-trivy 0.2.6`.
*   **Gestion des versions :** Fixer les GitHub Actions sur des **empreintes SHA complètes** plutôt que sur des tags de version, car ces derniers sont modifiables.
*   **Réponse aux incidents :** Considérer tous les secrets utilisés dans les pipelines ayant exécuté les versions compromises comme compromis et procéder à une rotation immédiate.
*   **Détection :** Bloquer le domaine `scan.aquasecurtiy[.]org` et l'IP `45.148.10[.]212`. Vérifier l'absence de dépôts nommés `tpcp-docs` sur les comptes GitHub associés aux pipelines.

---
[Source](https://thehackernews.com/2026/03/trivy-security-scanner-github-actions.html){:target="_blank"}
