---
title: 'GhostAction Compromises About 1,900 GitHub Accounts, Targets Over 30,000 Repositories'
date: 2026-10-15
permalink: /posts/2026/10/15/ghostaction-compromises-about-1900-github-accounts-targets-over-30000-repositories/
tags:
- veille-cyber
- hackernews
---
### GhostAction : Campagne d'attaques sur la chaîne d'approvisionnement GitHub

La campagne malveillante « GhostAction » cible l'infrastructure des développeurs sur GitHub en compromettant des comptes légitimes pour injecter des workflows d'automatisation malveillants. Cette campagne vise le vol massif de secrets CI/CD, d'identifiants cloud, de jetons de registres de paquets (npm, PyPI, DockerHub) et de clés API d'IA.

**Points clés :**
*   **Envergure :** La vague observée en octobre 2026 a touché environ 1 900 comptes et plus de 30 000 dépôts.
*   **Mode opératoire :** Utilisation de jetons d'accès personnel (PAT) volés ou d'identifiants issus de malwares de type « infostealer ». Les attaquants insèrent des fichiers YAML frauduleux (ex: `security-audit.yml`) pour automatiser l'extraction de données.
*   **Évolution :** Les payloads récents intègrent des fonctionnalités de scan de l'historique Git pour détecter des secrets précédemment enfouis, ainsi qu'une analyse contextuelle pour associer les clés AWS à leurs jetons d'accès secrets.
*   **Persistance :** Les attaquants ciblent à nouveau des victimes déjà compromises, exploitant le fait que de nombreux secrets n'ont pas été renouvelés (non-rotation).

**Vulnérabilités :**
*   Absence de rotation régulière des secrets après une compromission.
*   Utilisation de privilèges excessifs dans les workflows GitHub Actions.
*   Compromission des postes de travail des développeurs (source des PAT volés).
*   *Note : Aucune CVE spécifique n'est associée à cette campagne, car elle repose sur l'abus de fonctionnalités légitimes (GitHub Actions) plutôt que sur une faille logicielle.*

**Recommandations :**
*   **Rotation immédiate :** Révoquer et renouveler tous les secrets CI/CD, clés API et jetons d'accès dès qu'une activité suspecte est détectée.
*   **Sécurisation des accès :** Appliquer le principe du moindre privilège aux jetons PAT et aux workflows GitHub Actions.
*   **Monitoring :** Surveiller les fichiers de configuration `.github/workflows` pour détecter toute modification non autorisée ou l'ajout de workflows suspects.
*   **Hygiène des dépôts :** Nettoyer l'historique Git pour supprimer tout secret compromis qui pourrait être extrait par des outils automatisés.

---
[Source](https://thehackernews.com/2026/10/ghostaction-compromises-about-1900.html){:target="_blank"}
