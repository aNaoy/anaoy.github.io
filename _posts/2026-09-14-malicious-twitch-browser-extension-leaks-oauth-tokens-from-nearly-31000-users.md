---
title: 'Malicious Twitch Browser Extension Leaks OAuth Tokens From Nearly 31,000 Users'
date: 2026-09-14
permalink: /posts/2026/09/14/malicious-twitch-browser-extension-leaks-oauth-tokens-from-nearly-31000-users/
tags:
- veille-cyber
- hackernews
---
### Fuite massive de jetons OAuth via l'extension "JeetBot" sur Twitch

L'extension de navigateur « Twitch Enhanced Viewer | JeetBot », disponible sur Chrome et Firefox, a exposé les jetons d'authentification (OAuth) de près de 31 000 utilisateurs. Ces jetons, cruciaux pour la sécurité des comptes, étaient transmis en clair vers des serveurs proxy gérés par l'opérateur de l'outil sous couvert de contournement de restrictions régionales.

**Points clés :**
* **Impact :** Environ 31 000 utilisateurs touchés (30 000 sur Chrome, 604 sur Firefox).
* **Mécanisme :** L'extension injectait le jeton OAuth de l'utilisateur dans les paramètres d'URL lors des requêtes vers les serveurs proxy, permettant théoriquement aux opérateurs d'accéder aux comptes (chat, messages privés, paramètres).
* **Origine :** L'opérateur, Aleksandr Popov, a reconnu une erreur de conception et un manque de transparence dans la politique de confidentialité, tout en niant une intention malveillante.
* **Exemptions suspectes :** Une liste codée en dur de dix chaînes russes ne faisait pas l'objet de cette redirection de jeton, une mesure présentée comme un correctif pour des problèmes de lecture vidéo spécifiques.

**Vulnérabilités :**
* **Fuite de jetons d'authentification :** Envoi de jetons OAuth sensibles en clair dans des paramètres d'URL, les exposant directement dans les logs des serveurs proxy. Aucune CVE n'est associée à cette vulnérabilité spécifique, car il s'agit d'une pratique de conception non sécurisée au sein d'une extension tierce.

**Recommandations :**
* **Mise à jour immédiate :** Si vous utilisez l'extension « JeetBot », mettez-la à jour vers la version **85.8.7** ou supérieure, qui ne transmet plus les jetons OAuth.
* **Désinstallation :** En cas d'indisponibilité de la mise à jour, désinstallez l'extension immédiatement.
* **Réinitialisation des accès :** La mise à jour de l'extension ne révoque pas les jetons ayant déjà été compromis. Il est fortement conseillé de se déconnecter de Twitch et de changer son mot de passe ou de révoquer les autorisations d'applications tierces dans les paramètres du compte pour invalider les anciens jetons.

---
[Source](https://thehackernews.com/2026/09/malicious-twitch-browser-extension.html){:target="_blank"}
