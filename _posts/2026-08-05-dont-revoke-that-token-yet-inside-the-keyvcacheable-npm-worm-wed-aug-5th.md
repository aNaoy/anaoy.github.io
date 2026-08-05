---
title: 'Dont Revoke That Token Yet: Inside the keyv/cacheable npm Worm, (Wed, Aug 5th)'
date: 2026-08-05
permalink: /posts/2026/08/05/dont-revoke-that-token-yet-inside-the-keyvcacheable-npm-worm-wed-aug-5th/
tags:
- veille-cyber
- sans-isc
---
### Le ver informatique « keyv/cacheable » : un piège lors de la remédiation

Une campagne d'attaque sophistiquée a compromis les bibliothèques npm `keyv` et `cacheable`, transformant ces dépendances largement utilisées en un ver capable d'auto-propagation.

**Points clés**
*   **Propagation automatique :** Le malware utilise le jeton npm volé pour injecter un script malveillant dans d'autres paquets publiés par le compte compromis.
*   **Vecteur d'exécution élargi :** L'exécution ne nécessite pas de commande `npm install`. Des configurations IDE (`.vscode/tasks.json`, `.claude/settings.json`) déclenchent le code malveillant dès l'ouverture d'un répertoire dans l'éditeur.
*   **Mécanisme de « Dead-man’s switch » :** Le malware surveille la validité du jeton GitHub volé. Si celui-ci est révoqué (via une erreur 4xx), le script déclenche une charge utile arbitraire distante avant de s'effacer.
*   **Persistance :** Le programme s'installe en tant que service système (`systemd` ou `LaunchAgent`), se faisant passer pour un outil de surveillance de jeton légitime.

**Vulnérabilités**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque exploite des fonctionnalités légitimes (hooks `preinstall`, scripts de lancement IDE et jetons d'authentification) plutôt qu'une faille logicielle classique. La confiance aveugle envers les attestations SLSA et l'absence de modification du code source de la bibliothèque elle-même ont permis l'infection.

**Recommandations de réponse à incident**
L'ordre des actions est critique pour éviter le déclenchement de la charge utile :

1.  **Isoler immédiatement :** Couper l'accès réseau de la machine infectée. Cela bloque l'exfiltration et empêche le « dead-man’s switch » de détecter la révocation du jeton.
2.  **Préserver les preuves :** Copier les fichiers malveillants (`~/.config/gh-token-monitor/`, hooks IDE, service système) avant toute suppression.
3.  **Éradiquer :** Supprimer les fichiers de persistance, les hooks d'autostart et vider les caches de paquets.
4.  **Rotation sécurisée :** Une fois la menace éradiquée, révoquer et renouveler les jetons npm, GitHub, Cloud, Vault et secrets CI.
5.  **Reconstruction :** Réinstaller systématiquement les machines ayant confirmé une exécution, car le nettoyage manuel ne garantit pas une élimination complète.

Un outil de tri est mis à disposition par l'auteur pour identifier les dépendances transitives (`keyv`) et les indicateurs de persistance sur les postes de travail : [npm-incident-response](https://github.com/Securest8/npm-incident-response).

---
[Source](https://isc.sans.edu/diary/rss/33218){:target="_blank"}
