---
title: 'Battling Cryptojacking, Botnets, and IABs &#x5b;Guest Diary&#x5d;, (Thu, Jan 15th)'
date: 2026-01-15
permalink: /posts/2026/01/15/battling-cryptojacking-botnets-and-iabs-x5bguest-diaryx5d-thu-jan-15th/
tags:
- veille-cyber
- sans-isc
---
**Confrontation des Acteurs Malveillants : Cryptojacking, Botnets et Courtiers d'Accès Initial**

Les attaques observées sur un honeypot DShield révèlent des tactiques utilisées par des groupes organisés, incluant le cryptojacking et les botnets. Ces entités peuvent évoluer vers des services de "DDoS pour la location" ou la vente d'accès initiaux à des systèmes compromis, agissant ainsi comme des Courtiers d'Accès Initial (IAB). L'analyse précoce de ces activités, comme la reconnaissance du système, permet de mettre en place des mesures de défense avant que l'attaque ne porte ses fruits.

Un scénario typique observé débute par une attaque par pulvérisation de mots de passe sur SSH, suivie d'une énumération approfondie du système (informations sur le noyau, l'architecture, les processeurs, les GPU, les versions binaires, les informations de connexion). Cette phase vise à déterminer la pertinence du système pour un botnet ou à préparer l'installation de mécanismes de persistance. Les actions suivantes peuvent inclure la suppression de fichiers pour préparer l'installation de malware (identifié comme Trojan et Miner, avec des références suggérant une implication dans un botnet). La souche de ce malware provient souvent d'adresses IP chinoises d'un même ASN. Il est à noter que bien que certaines activités soient attribuées au groupe "Outlaw", d'autres peuvent représenter une évolution ou une spécialisation des rôles au sein du paysage de la cybercriminalité, avec des acteurs se concentrant sur l'accès initial, l'exploitation ou les actions post-exploitation.

**Points Clés :**

*   **Chaîne d'attaque fréquente :** Pulvérisation de mots de passe SSH -> Énumération du système -> Mécanismes de persistance via SSH -> Transfert de fichier malveillant.
*   **Organisation criminelle évoluée :** Les groupes cybercriminels se structurent de plus en plus comme des entreprises, avec une spécialisation des rôles (accès initial, exploitation, actions sur l'objectif).
*   **Importance de la détection précoce :** Identifier les signes de reconnaissance permet de réagir avant que l'attaque ne se développe.
*   **Cryptojacking et botnets comme menaces économiques :** Ces activités peuvent financer des opérations plus larges comme le DDoS pour la location.

**Vulnérabilités :**

*   **Accès SSH faible :** Les attaques par pulvérisation de mots de passe exploitent des combinaisons de noms d'utilisateur et de mots de passe faibles ou par défaut.
*   **Manque de segmentation réseau et d'isolation :** Un système compromis peut servir de tremplin pour attaquer d'autres parties du réseau.
*   **Vulnérabilités logicielles et systèmes obsolètes :** Les attaques automatisées ciblent souvent les systèmes non patchés.

**Recommandations :**

*   **Authentification forte :**
    *   Désactiver l'authentification par mot de passe pour SSH au profit de l'authentification par clé.
    *   Mettre en œuvre l'authentification multifacteur (MFA) pour les accès administratifs.
*   **Contrôles d'accès et défense en profondeur :**
    *   Utiliser TCP Wrappers (`/etc/hosts.allow`, `/etc/hosts.deny`) pour restreindre l'accès.
    *   Surveiller et alerter sur l'exécution rapide de commandes de reconnaissance courantes (ex: `uname`, `lscpu`, `w`, `top`).
    *   Détecter et enquêter sur les commandes de suppression ou de préparation à la persistance (ex: suppression récursive de répertoires `.ssh`, utilisation de `chattr`).
    *   Auditer régulièrement les comptes utilisateurs, les appartenances aux groupes et les attributions de privilèges.
*   **Surveillance et journalisation :**
    *   Centraliser les logs d'authentification, d'exécution de processus et réseau, avec une rétention minimale de 90 jours.
    *   Appliquer la surveillance de l'intégrité des fichiers (FIM) sur les fichiers critiques.
*   **Maintenance et réponse aux incidents :**
    *   Appliquer régulièrement les correctifs et gérer les vulnérabilités des systèmes et services exposés.
    *   Tester et exercer le plan de réponse aux incidents (IRP).
*   **Intelligence et Threat Hunting :**
    *   Investir dans la chasse aux menaces et le renseignement sur les menaces cybernétiques pour identifier et prédire les activités adverses.

---
[Source](https://isc.sans.edu/diary/rss/32632){:target="_blank"}
