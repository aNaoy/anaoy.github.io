---
title: 'New Gitea RCE Lets Repository Writers Plant a Git Hook to Run Shell Commands'
date: 2026-07-29
permalink: /posts/2026/07/29/new-gitea-rce-lets-repository-writers-plant-a-git-hook-to-run-shell-commands/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code à distance dans Gitea

Une vulnérabilité critique de type exécution de code à distance (RCE) a été découverte dans la plateforme Gitea, permettant à un utilisateur disposant de droits d'écriture sur un dépôt de compromettre le serveur en manipulant des hooks Git.

**Points clés :**
* **Mécanisme d'attaque :** En envoyant un patch malveillant via l'API `diffpatch`, un attaquant peut provoquer une collision de fichiers qui dépose un script exécutable dans le répertoire `.git/hooks` du serveur, déclenchant ainsi l'exécution de commandes arbitraires.
* **Accessibilité :** Bien que l'attaque nécessite des droits d'écriture, la configuration par défaut de Gitea autorise l'inscription libre, permettant à tout visiteur de créer un compte et d'exploiter la faille sans privilèges préalables.
* **Impact :** L'attaquant obtient les privilèges du compte système exécutant Gitea, ce qui peut mener à la compromission de secrets, de bases de données, d'identifiants OAuth et d'autres ressources internes.

**Vulnérabilité identifiée :**
* **CVE-2026-60004** (Score CVSS : 9.8). Concerne les versions 1.17 à 1.27.0.

**Recommandations :**
* **Mise à jour immédiate :** Passer à la version **1.27.1**, qui corrige la faille en modifiant la gestion des clones temporaires (le passage d'un clone "bare" à "non-bare" empêche l'écriture dans les hooks).
* **Durcissement de la configuration :** Désactiver l'inscription libre ("open registration") pour limiter les vecteurs d'attaque, bien que cela ne constitue pas un correctif complet contre les utilisateurs existants.
* **Vigilance accrue :** Surveiller les logs pour détecter toute activité suspecte sur les dépôts, étant donné qu'un PoC public est disponible.

---
[Source](https://thehackernews.com/2026/07/new-gitea-rce-lets-repository-writers.html){:target="_blank"}
