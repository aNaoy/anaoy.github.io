---
title: 'Match Group breach exposes data from Hinge, Tinder, OkCupid, and Match'
date: 2026-01-29
permalink: /posts/2026/01/29/match-group-breach-exposes-data-from-hinge-tinder-okcupid-and-match/
tags:
- veille-cyber
- bleepingcomp
---
**Fuite de données chez Match Group**

Match Group, l'entreprise mère de plateformes de rencontres populaires telles que Hinge, Tinder, OkCupid et Match.com, a subi une violation de données. Le groupe de menaces ShinyHunters a divulgué environ 1,7 Go de fichiers compressés, contenant prétendument 10 millions d'enregistrements d'utilisateurs et des documents internes.

Bien que l'enquête soit en cours avec des experts externes, Match Group affirme qu'il n'y a aucune indication que les identifiants de connexion, les informations financières ou les communications privées des utilisateurs aient été compromis. L'incident concerne une "quantité limitée de données utilisateur", et les individus concernés sont en cours de notification.

Cette attaque s'inscrit dans le cadre d'une campagne de phishing vocal plus large ciblant les comptes d'authentification unique (SSO) chez Okta, Microsoft et Google, visant plus d'une centaine d'organisations. Dans le cas de Match Group, les attaquants ont accédé aux données après avoir compromis un compte Okta SSO, leur donnant accès à des outils d'analyse marketing et à des services de stockage cloud. L'attaque a utilisé un domaine de phishing se faisant passer pour un portail interne de Match Group.

**Points Clés :**

*   **Nature de la fuite :** Données utilisateur limitées, documents internes.
*   **Volume de données :** Environ 1,7 Go compressé, 10 millions d'enregistrements présumés.
*   **Services affectés :** Hinge, Match, OkCupid.
*   **Attaque :** Campagne de phishing vocal (vishing) ciblant les comptes SSO, exploitant un compte Okta compromis.
*   **Accès :** Accès à des plateformes d'analyse marketing (AppsFlyer) et à des services de stockage cloud (Google Drive, Dropbox).
*   **Données *non* compromises (selon Match Group) :** Identifiants de connexion, informations financières, communications privées.

**Vulnérabilités / Vecteurs d'Attaque :**

*   **Phishing vocal (vishing) / Ingénierie sociale :** Technique principale utilisée pour tromper les utilisateurs et obtenir leurs identifiants SSO.
*   **Compromission de compte SSO (Okta) :** L'accès initial a été obtenu via la compromission d'un compte Okta.
*   **Domaine de phishing :** Utilisation d'un nom de domaine ressemblant à un portail interne légitime pour tromper les victimes.

**Recommandations :**

*   **Authentification Multi-Facteurs (MFA) résistante au phishing :** Utilisation de clés de sécurité FIDO2 ou de passkeys, qui sont plus sûres que l'authentification par SMS ou push.
*   **Politiques d'autorisation d'applications strictes :** Vérifier et contrôler les applications ayant accès aux ressources de l'entreprise.
*   **Surveillance des journaux :** Détecter les activités d'API anormales ou les enregistrements de périphériques non autorisés.
*   **Okta FastPass ou passkeys :** Pour renforcer l'authentification des employés utilisant Okta.
*   **Configuration des zones réseau et listes de contrôle d'accès aux locataires :** Limiter l'accès depuis des réseaux ou services anonymes souvent utilisés par les acteurs malveillants.
*   **Vérification des appels :** Des systèmes où les utilisateurs peuvent vérifier l'identité d'un représentant via une application mobile officielle.

---
[Source](https://www.bleepingcomputer.com/news/security/match-group-breach-exposes-data-from-hinge-tinder-okcupid-and-match/){:target="_blank"}
