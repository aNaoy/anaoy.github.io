---
title: 'BdThemes Supply Chain Attack Poisons JSON to Create Rogue WordPress Admins'
date: 2026-08-11
permalink: /posts/2026/08/11/bdthemes-supply-chain-attack-poisons-json-to-create-rogue-wordpress-admins/
tags:
- veille-cyber
- hackernews
---
### Attaque de chaîne d'approvisionnement via les API BdThemes

Des attaquants ont compromis l'écosystème du développeur WordPress **BdThemes** en infectant des fichiers JSON distants utilisés par plusieurs de leurs extensions. Cette attaque par empoisonnement de flux de données contourne les dépôts officiels, rendant la menace invisible au niveau du code source des plugins.

#### Points clés
*   **Méthode d'attaque :** Les attaquants ont obtenu un accès en écriture au bucket de stockage (DigitalOcean) utilisé par BdThemes pour afficher des bannières promotionnelles. Ils ont injecté des charges utiles malveillantes dans les fichiers JSON servis par l'API.
*   **Impact :** Une fois le fichier JSON chargé dans le tableau de bord WordPress (wp-admin), le script injecté s'exécute dans le navigateur de l'administrateur connecté.
*   **Actions malveillantes :** Création de comptes administrateurs factices, installation de web shells PHP, déploiement de backdoors (via les *mu-plugins* pour une persistance maximale) et dissimulation de la présence de comptes malveillants dans l'interface.
*   **Victimes :** Sept plugins, dont *Element Pack Addons for Elementor* (100 000+ installations) et *Ultimate Store Kit*.

#### Vulnérabilités
*   **XSS (Cross-Site Scripting) :** La faille réside dans le composant interne "Biggopti" qui traite les données JSON de l'API sans échappement client-side suffisant (Score CVSS : 5.4).

#### Recommandations
*   **Action immédiate :** Supprimer les plugins BdThemes affectés si cela n'a pas déjà été fait par WordPress.
*   **Audit de sécurité :** Vérifier les listes d'utilisateurs administrateurs à la recherche de comptes suspects (notamment ceux commençant par `bd_` suivis d'un hash, ou des comptes créés récemment).
*   **Nettoyage système :** Inspecter le répertoire `/wp-content/mu-plugins/` pour détecter tout script non autorisé ou backdoor.
*   **Mise à jour :** Rester en veille sur les communications officielles de WordPress concernant la réintégration de ces plugins après audit complet.

---
[Source](https://thehackernews.com/2026/08/bdthemes-supply-chain-attack-poisons.html){:target="_blank"}
