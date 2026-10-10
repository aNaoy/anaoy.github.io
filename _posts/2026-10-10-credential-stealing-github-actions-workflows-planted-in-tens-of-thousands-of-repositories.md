---
title: 'Credential-Stealing GitHub Actions Workflows Planted in Tens of Thousands of Repositories'
date: 2026-10-10
permalink: /posts/2026/10/10/credential-stealing-github-actions-workflows-planted-in-tens-of-thousands-of-repositories/
tags:
- veille-cyber
- hackernews
---
### La campagne GhostAction : compromission massive de dépôts GitHub

La campagne d'attaque à la chaîne d'approvisionnement **GhostAction** exploite des comptes de développeurs compromis pour injecter des workflows GitHub Actions malveillants dans des dizaines de milliers de dépôts. Les attaquants utilisent des jetons d'accès personnels (PAT) dérobés pour automatiser le déploiement de scripts malveillants se faisant passer pour des outils d'audit de sécurité.

**Points clés :**
* **Vecteur d'attaque :** Utilisation de comptes de contributeurs légitimes (souvent compromis via des infostealers) pour injecter du code dans les branches par défaut.
* **Méthode :** Les workflows malveillants (`security-audit.yml` ou `github_actions_security.yml`) scannent l'intégralité de l'arborescence et de l'historique Git à la recherche de secrets (AWS, API AI, DockerHub, etc.).
* **Exfiltration :** Les données récoltées sont envoyées en clair via HTTP vers une adresse IP contrôlée par les assaillants (`193.32.204[.]199`).
* **Ampleur :** Des centaines de comptes et des milliers de dépôts ont été infectés. Le risque s'étend aux forks et aux miroirs des dépôts compromis.
* **Vulnérabilité :** Aucune CVE spécifique n'est associée, il s'agit d'un abus de fonctionnalités légitimes de GitHub Actions rendu possible par le vol de jetons d'authentification.

**Recommandations :**
* **Audit immédiat :** Rechercher la présence des fichiers `security-audit.yml` ou `github_actions_security.yml` dans tous les dépôts depuis le 31 août 2026.
* **Réponse à incident :** En cas de détection, considérer le compte comme compromis. Révoquer immédiatement tous les jetons (PAT, API keys, CI/CD secrets) associés.
* **Assainissement :** Supprimer les workflows malveillants sur toutes les branches et vérifier l'intégrité des forks et des dépôts descendants.
* **Rotation des secrets :** Procéder à une rotation systématique de toutes les clés d'API et identifiants exposés dans le code ou l'historique Git.

---
[Source](https://thehackernews.com/2026/10/credential-stealing-github-actions.html){:target="_blank"}
