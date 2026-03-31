---
title: 'Axios Supply Chain Attack Pushes Cross-Platform RAT via Compromised npm Account'
date: 2026-03-31
permalink: /posts/2026/03/31/axios-supply-chain-attack-pushes-cross-platform-rat-via-compromised-npm-account/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement Axios : Un RAT multiplateforme déployé

Une attaque par chaîne d'approvisionnement a compromis le client HTTP **Axios** (versions 1.14.1 et 0.30.4) sur le registre npm, après le piratage du compte d'un mainteneur principal. L'attaque injecte une dépendance malveillante nommée `plain-crypto-js` (version 4.2.1), utilisée comme vecteur pour déployer un cheval de Troie d'accès à distance (RAT).

**Points clés :**
*   **Méthode d'attaque :** Utilisation d'un jeton d'accès npm volé pour publier des versions altérées sans modifier le code source d'Axios lui-même, contournant ainsi les revues de code classiques.
*   **Action malveillante :** Un script `postinstall` exécute un dropper Node.js qui télécharge une charge utile adaptée au système cible (macOS, Windows ou Linux).
*   **Évasion :** Le malware supprime ses traces après l'exécution et restaure un `package.json` sain pour éviter toute détection forensique.
*   **Attribution possible :** Les techniques observées présentent des similitudes avec le groupe nord-coréen UNC1069.
*   **Propagation élargie :** D'autres packages (`@shadanai/openclaw`, `@qqbrowser/openclaw-qbot`) ont été identifiés comme distribuant le même malware via des dépendances intégrées (vendoring).

**Vulnérabilités :**
*   Pas de CVE spécifique attribuée, mais l'incident exploite la confiance accordée aux dépendances npm et aux scripts `postinstall` exécutés automatiquement lors de l'installation.

**Recommandations :**
*   **Correction immédiate :** Rétrograder Axios vers les versions 1.14.0 ou 0.30.3.
*   **Nettoyage :** Supprimer `plain-crypto-js` du répertoire `node_modules`.
*   **Réponse sur incident :** Si des artefacts (`/Library/Caches/com.apple.act.mond`, `%PROGRAMDATA%\wt.exe`, `/tmp/ld.py`) sont détectés, considérer le système comme compromis, procéder à une rotation immédiate de tous les secrets/identifiants et auditer les pipelines CI/CD.
*   **Réseau :** Bloquer tout trafic sortant vers le domaine C2 `sfrclak[.]com`.

---
[Source](https://thehackernews.com/2026/03/axios-supply-chain-attack-pushes-cross.html){:target="_blank"}
