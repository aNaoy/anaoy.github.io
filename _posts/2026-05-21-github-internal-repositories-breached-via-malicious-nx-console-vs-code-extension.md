---
title: 'GitHub Internal Repositories Breached via Malicious Nx Console VS Code Extension'
date: 2026-05-21
permalink: /posts/2026/05/21/github-internal-repositories-breached-via-malicious-nx-console-vs-code-extension/
tags:
- veille-cyber
- hackernews
---
### Infiltration de GitHub via une extension VS Code piégée

GitHub a confirmé une intrusion dans ses dépôts internes causée par l'installation d'une version malveillante de l'extension VS Code « Nx Console » (`nrwl.angular-console`). Cette attaque, attribuée au groupe cybercriminel TeamPCP, s'inscrit dans une série de compromissions de la chaîne d'approvisionnement logicielle (notamment via l'attaque TanStack).

**Points clés :**
* **Vecteur d'attaque :** Le poste de travail d'un développeur de l'extension Nx Console a été compromis, permettant aux attaquants d'injecter un code malveillant dans l'extension.
* **Rapidité d'action :** La version piégée n'est restée disponible sur le Visual Studio Marketplace que 18 minutes, ce qui a suffi pour exfiltrer des données sensibles (GitHub, AWS, npm, 1Password, Claude Code) chez les développeurs l'ayant mise à jour.
* **Impact :** Environ 3 800 dépôts internes de GitHub ont été consultés. GitHub a révoqué les accès compromis et contraint la rotation des secrets.
* **Vulnérabilité systémique :** Le mécanisme de mise à jour automatique des extensions VS Code permet une propagation immédiate et non contrôlée de code malveillant dès la publication d'une version compromise par un éditeur légitime.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée pour ce cas précis ; l'incident repose sur l'exploitation de la confiance accordée aux extensions tierces et sur l'absence de vérification rigoureuse lors des mises à jour automatiques des IDE.

**Recommandations :**
* **Éditeurs de logiciels :** Renforcer la sécurité des accès aux comptes de publication sur les marketplaces d'extensions et implémenter des mesures de protection contre le détournement de comptes développeurs.
* **Développeurs :**
    * Limiter les privilèges des extensions VS Code si possible.
    * Prêter une attention accrue aux notifications de mise à jour automatique.
    * Réviser régulièrement la gestion des secrets stockés localement (coffres-forts, configurations d'outils d'IA).
* **Écosystèmes :** Réévaluer la confiance aveugle envers le processus de mise à jour automatique des marketplaces, qui nécessite des mécanismes de validation plus stricts pour contrer les attaques de type "supply chain".

---
[Source](https://thehackernews.com/2026/05/github-internal-repositories-breached.html){:target="_blank"}
