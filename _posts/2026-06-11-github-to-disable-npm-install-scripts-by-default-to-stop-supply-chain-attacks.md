---
title: 'GitHub to Disable npm Install Scripts by Default to Stop Supply Chain Attacks'
date: 2026-06-11
permalink: /posts/2026/06/11/github-to-disable-npm-install-scripts-by-default-to-stop-supply-chain-attacks/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la sécurité de la chaîne d'approvisionnement npm

GitHub a annoncé des changements majeurs pour la version 12 du gestionnaire de paquets npm, visant à neutraliser les attaques par chaîne d'approvisionnement exploitant l'exécution automatique de scripts lors de l'installation.

**Points clés :**
* **Désactivation par défaut :** Les scripts de cycle de vie (ex: `preinstall`, `install`, `postinstall`) ne s'exécuteront plus automatiquement.
* **Surface d'attaque réduite :** La modification bloque l'exécution de code arbitraire provenant de dépendances compromises ou malveillantes au sein de l'arbre des dépendances.
* **Contrôle accru :** L'exécution de scripts, la résolution de dépendances Git et les URLs distantes nécessiteront désormais une approbation explicite de l'utilisateur.

**Vulnérabilités traitées :**
* **Exécution de code arbitraire (RCE) :** Utilisation des hooks de cycle de vie npm pour compromettre les machines des développeurs ou les environnements d'intégration continue (CI).
* **Détournement de Git :** Risque lié aux fichiers `.npmrc` malveillants pouvant outrepasser les mesures de sécurité existantes (comme `--ignore-scripts`) lors de l'installation de dépendances Git.

**Recommandations :**
* **Mise à jour :** Passer à npm version 11.16.0 ou supérieure pour identifier les scripts via les avertissements générés.
* **Audit et approbation :** Utiliser la commande `npm approve-scripts --allow-scripts-pending` pour examiner les paquets, valider uniquement ceux de confiance et mettre à jour le fichier `package.json` en conséquence.
* **Sécurisation proactive :** Tirer parti du paramètre `min-release-age` pour rejeter automatiquement les paquets trop récents, limitant ainsi l'exposition aux attaques « typosquatting » ou aux paquets malveillants fraîchement publiés.

---
[Source](https://thehackernews.com/2026/06/github-to-disable-npm-install-scripts.html){:target="_blank"}
