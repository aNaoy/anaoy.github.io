---
title: 'Second Sha1-Hulud Wave Affects 25,000+ Repositories via npm Preinstall Credential Theft'
date: 2025-11-24
permalink: /posts/2025/11/24/second-sha1-hulud-wave-affects-25000-repositories-via-npm-preinstall-credential-theft/
tags:
- veille-cyber
- hackernews
---
## Deuxième vague de Sha1-Hulud : Vol de secrets et sabotage via npm

Une nouvelle campagne de compromission de la chaîne d'approvisionnement logicielle, baptisée Sha1-Hulud, cible le registre npm. Cette attaque, apparue entre le 21 et le 23 novembre 2025, exploite des paquets npm malveillants pour dérober des informations sensibles et potentiellement détruire des données.

**Points Clés :**

*   La campagne est une nouvelle variante de l'attaque Shai-Hulud, révélée en septembre 2025.
*   Des centaines de paquets npm ont été compromis, affectant potentiellement plus de 25 000 dépôts.
*   Les paquets malveillants sont conçus pour s'exécuter lors de la phase de préinstallation (`preinstall` script dans `package.json`).
*   L'objectif principal est le vol de secrets (jetons npm, identifiants cloud, variables d'environnement) à l'aide d'outils comme TruffleHog.
*   Les informations volées sont exfiltrées vers des dépôts GitHub sous une description spécifique ("Sha1-Hulud: The Second Coming").
*   Une nouvelle fonctionnalité agressive dans cette vague est la capacité du malware à tenter d'effacer l'intégralité du répertoire personnel de la victime si l'exfiltration échoue, marquant un passage du vol de données au sabotage.
*   Le malware cherche également à obtenir des privilèges root en manipulant le système de fichiers de l'hôte via un conteneur Docker.

**Vulnérabilités :**

Aucune CVE spécifique n'est mentionnée dans l'article, mais la vulnérabilité réside dans l'exécution de code arbitraire via les scripts de préinstallation des paquets npm compromis, ainsi que dans l'exploitation potentielle des mécanismes d'automatisation de GitHub Actions.

**Recommandations :**

*   Scanner tous les points d'accès pour détecter la présence de paquets affectés.
*   Supprimer immédiatement les versions compromises des paquets.
*   Régénérer tous les identifiants et secrets potentiellement exposés.
*   Auditer les dépôts pour détecter des mécanismes de persistance, en particulier dans les répertoires `.github/workflows/`.

---
[Source](https://thehackernews.com/2025/11/second-sha1-hulud-wave-affects-25000.html){:target="_blank"}
