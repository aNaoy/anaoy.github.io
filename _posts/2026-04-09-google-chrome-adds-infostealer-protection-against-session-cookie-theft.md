---
title: 'Google Chrome adds infostealer protection against session cookie theft'
date: 2026-04-09
permalink: /posts/2026/04/09/google-chrome-adds-infostealer-protection-against-session-cookie-theft/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation des sessions : Google Chrome déploie le DBSC

Google a intégré la technologie **Device Bound Session Credentials (DBSC)** dans Chrome 146 sur Windows, une solution visant à neutraliser les logiciels malveillants de type « infostealer » qui dérobent les cookies de session. Cette fonctionnalité lie cryptographiquement une session utilisateur au matériel spécifique de la machine (puce TPM sur Windows ou Secure Enclave sur macOS).

**Points clés :**
*   **Liaison matérielle :** Les clés privées générées par la puce de sécurité ne peuvent pas être exportées, rendant les cookies volés inutilisables par les attaquants en dehors de la machine d'origine.
*   **Inutilisabilité immédiate :** Si un attaquant exfiltre un cookie de session, il ne pourra pas prouver la possession de la clé privée associée, entraînant l'expiration immédiate du jeton.
*   **Protection de la vie privée :** Le protocole DBSC utilise des clés distinctes par session, empêchant le suivi ou la corrélation des activités des utilisateurs entre différents sites ou sessions.
*   **Standardisation :** Développé avec Microsoft, le DBSC est proposé comme un standard web ouvert (W3C), permettant une implémentation progressive par les développeurs web.

**Vulnérabilités ciblées :**
*   **Vol de cookies de session (Session Hijacking) :** Les logiciels malveillants de type « infostealer » (ex: LummaC2) exploitent l'accès au système de fichiers et à la mémoire pour extraire des jetons d'authentification valides, contournant ainsi les mécanismes d'authentification classiques (mots de passe, 2FA). *Note : Aucune CVE spécifique n'est associée à cette faille de conception, le vol de cookies étant inhérent au stockage logiciel des jetons.*

**Recommandations :**
*   **Pour les développeurs web :** Intégrer les points de terminaison (endpoints) d'enregistrement et de rafraîchissement DBSC sur les serveurs back-end pour protéger les sessions des utilisateurs.
*   **Pour les utilisateurs :** Maintenir Google Chrome à jour vers la version 146 ou supérieure pour bénéficier de cette protection matérielle.
*   **Adoption du standard :** Encourager les plateformes et services en ligne à adopter le protocole DBSC pour renforcer la sécurité globale des accès aux comptes.

---
[Source](https://www.bleepingcomputer.com/news/security/google-chrome-adds-infostealer-protection-against-session-cookie-theft/){:target="_blank"}
