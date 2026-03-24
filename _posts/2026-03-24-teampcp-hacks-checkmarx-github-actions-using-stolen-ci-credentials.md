---
title: 'TeamPCP Hacks Checkmarx GitHub Actions Using Stolen CI Credentials'
date: 2026-03-24
permalink: /posts/2026/03/24/teampcp-hacks-checkmarx-github-actions-using-stolen-ci-credentials/
tags:
- veille-cyber
- hackernews
---
### Attaque sur la chaîne d'approvisionnement : Le groupe TeamPCP compromet les actions GitHub de Checkmarx

Le groupe cybercriminel TeamPCP a étendu sa campagne d'attaques sur la chaîne d'approvisionnement, ciblant cette fois les outils GitHub Actions de Checkmarx après avoir infiltré les scanners Trivy d'Aqua Security. L'attaque exploite des identifiants volés pour injecter des logiciels malveillants de type "infostealer" destinés à récolter des secrets sensibles.

**Points clés :**
*   **Mode opératoire :** Les attaquants forcent le déplacement de tags (`force-push`) vers des commits contenant un script malveillant (`setup.sh`). Ils utilisent des domaines de type "typosquatting" pour masquer leurs communications réseau.
*   **Vecteurs d'infection :** En plus des workflows GitHub Actions, des extensions Open VSX (`ast-results` et `cx-dev-assist`) ont été piégées.
*   **Capacités du malware :** Le vol de secrets (AWS, Azure, GCP, Kubernetes, tokens GitHub) permet une escalade latérale, facilitant de futures compromissions en cascade.
*   **Persistance :** Sur les systèmes hors CI, le malware installe un service `systemd` avec un mécanisme de mise à jour distante.

**Vulnérabilité associée :**
*   **CVE-2026-33634** (Score CVSS : 9.4) : Identifiant lié à l'incident initial sur Trivy, servant de base à la propagation actuelle.

**Recommandations de sécurité :**
*   **Rotation immédiate :** Réinitialiser tous les secrets, tokens et identifiants cloud potentiellement exposés par les runners CI.
*   **Audit technique :** Rechercher dans les logs la présence de `tpcp.tar.gz`, de connexions vers `checkmarx[.]zone`, ou de dépôts suspects nommés `tpcp-docs` / `docs-tpcp`.
*   **Durcissement des workflows :** Épingler systématiquement les GitHub Actions à des **SHA de commit complets** plutôt qu'à des versions (tags), ces derniers pouvant être modifiés par les attaquants.
*   **Contrôle réseau :** Restreindre les communications sortantes des runners CI et implémenter l'IMDSv2 pour limiter l'exposition des métadonnées d'instance.
*   **Veille :** Surveiller les accès aux services cloud et les activités inhabituelles sur les dépôts de code.

---
[Source](https://thehackernews.com/2026/03/teampcp-hacks-checkmarx-github-actions.html){:target="_blank"}
