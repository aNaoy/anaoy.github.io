---
title: 'Megalodon GitHub Attack Targets 5,561 Repos with Malicious CI/CD Workflows'
date: 2026-05-22
permalink: /posts/2026/05/22/megalodon-github-attack-targets-5561-repos-with-malicious-cicd-workflows/
tags:
- veille-cyber
- hackernews
---
### Campagne Megalodon : Une menace massive sur les workflows CI/CD

La campagne automatisée "Megalodon" a compromis plus de 5 500 dépôts GitHub en l'espace de six heures. Utilisant des comptes jetables et des identités usurpées, les attaquants ont injecté des workflows GitHub Actions malveillants visant à exfiltrer des secrets et des identifiants sensibles depuis les pipelines CI/CD.

#### Points clés
*   **Mode opératoire :** Injection de commits malveillants contenant des payloads Bash encodés en Base64.
*   **Amplitude :** 5 718 commits poussés vers 5 561 dépôts GitHub distincts.
*   **Cible :** Récupération massive de secrets (AWS, Google Cloud, Azure, Kubernetes, SSH, clés API, tokens GitHub/GitLab).
*   **Tactiques :** Utilisation de deux variantes (SysDiag pour une exécution à chaque push/PR et Optimize-Build via `workflow_dispatch` pour une exécution ciblée).
*   **Contexte élargi :** Cette attaque s'inscrit dans une tendance plus large de compromissions de la chaîne d'approvisionnement logicielle, incluant les activités du groupe "TeamPCP" et le ver "Mini Shai-Hulud".

#### Vulnérabilités exploitées
*   **Abus de configuration CI/CD :** Exploitation de la confiance accordée aux workflows automatisés.
*   **Compromission des accès :** Utilisation de PATs (Personal Access Tokens) compromis ou de clés de déploiement pour injecter du code.
*   **Absence de cloisonnement :** Accès trop permissif des pipelines aux secrets de production et clés de cloud (IMDSv2, tokens OIDC).

#### Recommandations
*   **Sécurisation des accès :** Révoquer et renouveler les tokens d'accès (PATs) et les secrets CI/CD compromis.
*   **Adoption de "Trusted Publishing" :** Privilégier les méthodes de publication sécurisées (notamment sur npm) pour réduire la dépendance aux tokens à longue durée de vie contournant le 2FA.
*   **Audit des workflows :** Examiner régulièrement les fichiers `.github/workflows` pour détecter des modifications suspectes ou l'ajout de payloads encodés.
*   **Principe du moindre privilège :** Restreindre strictement les permissions accordées aux tokens GitHub (GITHUB_TOKEN) et aux rôles IAM utilisés par les runners CI/CD.
*   **Surveillance :** Surveiller les journaux d'exécution des workflows pour détecter des appels inattendus vers des serveurs C2 (ex: l'IP identifiée 216.126.225.129).

---
[Source](https://thehackernews.com/2026/05/megalodon-github-attack-targets-5561.html){:target="_blank"}
