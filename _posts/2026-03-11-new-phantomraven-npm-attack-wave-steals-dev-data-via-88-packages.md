---
title: 'New PhantomRaven NPM attack wave steals dev data via 88 packages'
date: 2026-03-11
permalink: /posts/2026/03/11/new-phantomraven-npm-attack-wave-steals-dev-data-via-88-packages/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne PhantomRaven : Recrudescence d'attaques sur NPM

La campagne malveillante « PhantomRaven » continue de viser l'écosystème NPM, ayant déployé 88 paquets suspects entre novembre 2025 et février 2026. Utilisant des techniques de « typosquatting » pour usurper des projets populaires (comme Babel ou GraphQL Codegen), les attaquants ciblent les développeurs JavaScript pour exfiltrer des données sensibles.

**Points clés :**
* **Technique d'évasion :** Utilisation de dépendances dynamiques distantes (RDD). Le fichier `package.json` pointe vers une URL externe, permettant d'exécuter du code malveillant sans l'inclure directement dans le paquet, contournant ainsi les analyses automatisées.
* **Données visées :** Configuration Git (`.gitconfig`), fichiers NPM (`.npmrc`), variables d'environnement, jetons CI/CD (GitHub, GitLab, Jenkins, CircleCI) et informations système (IP, OS, version de Node).
* **Infrastructure :** Les attaquants utilisent des domaines contenant le mot "artifact" hébergés sur AWS EC2, sans certificat TLS.
* **Persistance :** Malgré une faible sophistication technique, la campagne demeure active grâce à une rotation fréquente des comptes NPM et des modifications mineures des métadonnées.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car l'attaque repose sur une exploitation légitime du fonctionnement des dépendances NPM (Remote Dynamic Dependencies) plutôt que sur une faille logicielle classique.

**Recommandations :**
* **Vérification rigoureuse :** Valider systématiquement la légitimité et la réputation des bibliothèques avant toute installation.
* **Prudence avec l'IA :** Éviter de copier-coller aveuglément des recommandations de noms de paquets fournies par des outils d'IA ou des sources non vérifiées.
* **Contrôle des dépendances :** Auditer régulièrement les fichiers `package.json` pour identifier des dépendances suspectes pointant vers des sources externes non reconnues.

---
[Source](https://www.bleepingcomputer.com/news/security/new-phantomraven-npm-attack-wave-steals-dev-data-via-88-packages/){:target="_blank"}
