---
title: 'New Shai-Hulud attack trojanizes 19 science-focused PyPI packages'
date: 2026-06-09
permalink: /posts/2026/06/09/new-shai-hulud-attack-trojanizes-19-science-focused-pypi-packages/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque de chaîne d'approvisionnement « Shai-Hulud » sur PyPI

Une nouvelle vague de cyberattaques, baptisée « Shai-Hulud », a compromis 19 paquets Python populaires (notamment des outils de bioinformatique comme *Dynamo*, *Spateo* et *CoolBox*), totalisant des centaines de milliers de téléchargements. Les attaquants ont injecté des scripts malveillants dans 37 versions de ces paquets pour dérober des secrets de développement.

**Points clés :**
*   **Mécanisme d'infection :** L'installation du paquet dépose un fichier `*-setup.pth` qui exécute automatiquement une charge utile JavaScript (`_index.js`) lors du démarrage de Python, utilisant le runtime *Bun* pour s'exécuter.
*   **Objectif :** Exfiltration massive de secrets (clés AWS/GCP/Azure, jetons GitHub, identifiants Docker, fichiers `.env`, clés SSH, historique shell, etc.).
*   **Persistance et évasion :** Le malware utilise des services `systemd` (Linux) ou `LaunchAgents` (macOS) et vérifie la présence d'outils de sécurité pour s'auto-protéger.
*   **Exfiltration :** Utilisation de dépôts GitHub créés automatiquement ou via des requêtes HTTPS camouflées vers l'API d'Anthropic.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique n'ait été assignée à cette campagne, elle exploite la nature permissive des fichiers `.pth` dans Python, qui permettent une exécution arbitraire de code dès le lancement de l'interpréteur.

**Recommandations :**
*   **Rotation immédiate :** Si ces paquets ont été installés, réinitialisez l'ensemble de vos secrets (clés API, jetons, mots de passe) et restaurez vos environnements à partir de sauvegardes saines.
*   **Détection :** Surveillez la présence de fichiers `.pth` exécutables dans vos dépendances Python et bloquez les téléchargements inattendus du runtime *Bun* depuis GitHub.
*   **Analyse comportementale :** Surveillez les chaînes de processus suspectes où Python tente d'exécuter `bun` ou des fichiers `.js` via le runtime Bun dans vos environnements CI/CD ou stations de travail.

---
[Source](https://www.bleepingcomputer.com/news/security/new-shai-hulud-attack-trojanizes-19-science-focused-pypi-packages/){:target="_blank"}
