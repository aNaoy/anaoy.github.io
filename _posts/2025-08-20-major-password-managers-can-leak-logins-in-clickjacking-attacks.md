---
title: 'Major password managers can leak logins in clickjacking attacks'
date: 2025-08-20
permalink: /posts/2025/08/20/major-password-managers-can-leak-logins-in-clickjacking-attacks/
tags:
- veille-cyber
- bleepingcomp
---
## Fuite de données via Clickjacking : Les gestionnaires de mots de passe en danger

Des vulnérabilités de clickjacking non corrigées affectent plusieurs gestionnaires de mots de passe populaires, potentiellement utilisés par des dizaines de millions de personnes. Ces failles pourraient permettre à des acteurs malveillants de voler des identifiants de connexion, des codes d'authentification à deux facteurs et des détails de cartes de crédit.

L'exploitation se fait en incitant l'utilisateur à visiter une page web compromise où des éléments HTML invisibles sont superposés à l'interface du gestionnaire de mots de passe. Lorsque l'utilisateur pense interagir avec des éléments légitimes, il déclenche en réalité des fonctions de remplissage automatique qui divulguent des informations sensibles.

### Points Clés :

*   **Technique d'attaque :** Utilisation de scripts sur des sites malveillants pour masquer le menu de remplissage automatique du gestionnaire de mots de passe via des manipulations d'opacité, de superpositions ou des astuces sur les événements de pointeur.
*   **Ciblage :** Des éléments intrusifs (bannières de cookies, pop-ups) sont ajoutés pour que les clics de l'utilisateur activent les contrôles cachés du gestionnaire de mots de passe, remplissant ainsi les formulaires avec des données sensibles.
*   **Adaptabilité :** Un script universel peut identifier le gestionnaire de mots de passe actif et adapter l'attaque en temps réel.

### Vulnérabilités :

La recherche a démontré que les variantes basées sur navigateur des gestionnaires de mots de passe suivants sont affectées :

*   1Password 8.11.4.27
*   Bitwarden 2025.7.0
*   Enpass 6.11.6 (une correction partielle a été implémentée dans la version 6.11.4.2)
*   iCloud Passwords 3.1.25
*   LastPass 4.146.3
*   LogMeOnce 7.12.4

Aucun identifiant CVE spécifique n'est mentionné dans l'article.

### Réponses des Vendeurs :

*   **1Password :** A rejeté le rapport, le considérant comme "hors périmètre/informatif".
*   **LastPass :** A marqué le rapport comme "informatif".
*   **Bitwarden :** A reconnu les problèmes mais a minimisé leur gravité. La version 2025.8.0, en cours de déploiement, corrigent les failles.
*   **LogMeOnce :** N'a pas répondu aux tentatives de communication.
*   **Vendors ayant corrigé :** Dashlane (v6.2531.1), NordPass, ProtonPass, RoboForm, Keeper (v17.2.0).

### Recommandations :

*   **Désactiver la fonction de remplissage automatique :** Jusqu'à ce que des correctifs soient disponibles, il est conseillé aux utilisateurs de désactiver cette fonction dans leurs gestionnaires de mots de passe.
*   **Utiliser la copie/coller :** Privilégier la méthode de copier-coller pour saisir les informations d'identification.
*   **Mettre à jour :** S'assurer d'utiliser les versions les plus récentes des logiciels de gestion de mots de passe.

---
[Source](https://www.bleepingcomputer.com/news/security/major-password-managers-can-leak-logins-in-clickjacking-attacks/){:target="_blank"}
