---
title: 'Popular WordPress Plugin Scripts Tampered to Plant Hidden Backdoors on Sites'
date: 2026-06-15
permalink: /posts/2026/06/15/popular-wordpress-plugin-scripts-tampered-to-plant-hidden-backdoors-on-sites/
tags:
- veille-cyber
- hackernews
---
### Attaque par chaîne d'approvisionnement via des plugins WordPress populaires

Des attaquants ont compromis les fichiers JavaScript officiels des plugins WordPress **PushEngage**, **OptinMonster** et **TrustPulse** (développés par *Awesome Motive*). En injectant du code malveillant dans ces scripts, les assaillants ont pu prendre le contrôle total des sites web utilisant ces extensions.

**Mécanisme d'attaque :**
Le script malveillant ne s'activait que lorsqu'un administrateur WordPress était connecté au site. Une fois le script exécuté via la session de l'administrateur, il procédait automatiquement aux actions suivantes :
* Création d'un compte administrateur pirate.
* Installation d'un plugin masqué agissant comme un *web shell* pour permettre l'exécution de commandes à distance.
* Exfiltration des informations de connexion vers un domaine malveillant (`tidio[.]cc`).

**Vulnérabilités :**
* Le vecteur d'entrée initial suspecté est une faille dans le plugin de sauvegarde **UpdraftPlus** (CVE-2022-10795, note de sévérité 8.1), permettant un contournement d'authentification.

**Points clés :**
* Plus de 1,2 million de sites potentiellement exposés par ces plugins.
* L'attaque était ciblée, orchestrée et planifiée (domaine de secours créé des semaines auparavant).
* La persistance est élevée : supprimer le plugin visible ne suffit pas, car des accès administrateurs ou des portes dérobées supplémentaires peuvent subsister sur le serveur.

**Recommandations :**
1. **Ne pas se fier au tableau de bord :** Le backdoor est conçu pour rester invisible. Effectuer impérativement une analyse côté serveur des fichiers.
2. **Recherche d'IoC (Indicateurs de compromission) :** Inspecter le répertoire `wp-content/plugins` à la recherche de dossiers suspects comme `content-delivery-helper` ou `database-optimizer`.
3. **Audit des comptes :** Supprimer tout compte administrateur inconnu, en particulier ceux nommés `developer_api1` ou commençant par `dev_`.
4. **Analyse des logs :** Rechercher dans les accès serveurs (12 au 14 juin) des requêtes vers le domaine `tidio[.]cc` ou l'adresse IP `84.201.6.54`.
5. **Nettoyage complet en cas d'infection :** En cas de détection, effectuer une rotation immédiate de tous les mots de passe administrateur, clés API, identifiants de base de données et des clés secrètes (*salts*) présentes dans le fichier `wp-config.php`.
6. **Mise à jour :** S'assurer que le plugin UpdraftPlus est à jour pour corriger les vulnérabilités connues.

---
[Source](https://thehackernews.com/2026/06/popular-wordpress-plugin-scripts.html){:target="_blank"}
