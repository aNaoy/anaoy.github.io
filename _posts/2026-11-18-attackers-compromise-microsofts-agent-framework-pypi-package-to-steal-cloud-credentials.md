---
title: 'Attackers Compromise Microsofts Agent Framework PyPI Package to Steal Cloud Credentials'
date: 2026-11-18
permalink: /posts/2026/11/18/attackers-compromise-microsofts-agent-framework-pypi-package-to-steal-cloud-credentials/
tags:
- veille-cyber
- hackernews
---
### Compromission du package PyPI « agent-framework » de Microsoft

Le package Python `agent-framework`, utilisé pour l'orchestration d'agents IA, a été compromis le 17 novembre 2026 par l'injection de versions malveillantes (1.26.1 et 1.26.2). Ces versions intègrent un logiciel espion capable de dérober des identifiants cloud et des jetons d'accès dès le démarrage de l'interpréteur Python. Aucune CVE n'a été attribuée à ce jour.

**Points clés :**
*   **Persistance immédiate :** L'installation dépose un fichier `.pth` dans `site-packages`, garantissant l'exécution du code malveillant à chaque lancement de Python, même sans importation explicite du framework.
*   **Vol de données étendu :** Le malware exfiltre des variables d'environnement, des fichiers de configuration (Azure CLI, `.npmrc`, `.git-credentials`, etc.), ainsi que des jetons d'identité (Managed Identity, OIDC) vers une adresse `webhook.site`.
*   **Escalade des privilèges :** Le script interroge activement les services de métadonnées (IMDS) et les endpoints d'identité pour générer de nouveaux jetons d'accès, rendant inutile la simple rotation des secrets statiques.

**Recommandations :**
*   **Remédiation immédiate :** Isolez les systèmes infectés, supprimez les versions 1.26.1/1.26.2 et revenez à la version 1.26.0.
*   **Audit de compromission :** Recherchez dans vos logs DNS/Proxy toute requête vers `webhook.site/d381fd80-ec62-42ad-8f5c-d1b15103c9bb`.
*   **Rotation proactive :** Révoquez et régénérez l'ensemble des identifiants, jetons Azure DevOps, tokens GitHub Actions et identités managées présents sur les machines ayant utilisé les versions compromises.
*   **Surveillance :** Analysez les logs d'activité et de connexion Azure à la recherche d'activités suspectes liées aux identités compromises.

---
[Source](https://thehackernews.com/2026/11/attackers-compromise-microsofts-agent.html){:target="_blank"}
