---
title: 'SimpleHelp bug lets hackers create rogue remote support accounts'
date: 2026-06-16
permalink: /posts/2026/06/16/simplehelp-bug-lets-hackers-create-rogue-remote-support-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans SimpleHelp : contournement d'authentification via OIDC

Une faille critique dans le logiciel de gestion à distance SimpleHelp permet à des attaquants non authentifiés de créer des comptes techniciens privilégiés en exploitant le protocole OpenID Connect (OIDC).

**Points clés :**
*   **Vulnérabilité :** CVE-2026-48558.
*   **Risque :** Un attaquant peut créer un compte administrateur et accéder aux terminaux gérés, exécuter des scripts et contourner l'authentification multifacteur (MFA).
*   **Cibles :** Versions 5.5.15 et antérieures, ainsi que les versions 6.0 pré-version.
*   **Conditions d'exploitation :** Le serveur doit utiliser OIDC, avoir un groupe de techniciens associé et l'option « Allow group authenticated logins » activée. Environ 7,2 % des 14 000 serveurs exposés publiquement seraient concernés.

**Recommandations :**
*   **Correctif immédiat :** Mettre à jour vers les versions 5.5.16 ou 6.0RC2.
*   **Atténuation :** Si la mise à jour est impossible, restreindre l'accès aux interfaces de connexion via des listes d'adresses IP autorisées.
*   **Surveillance :** Inspecter les logs (`/opt/SimpleHelp/logs/server.log`) à la recherche de créations de comptes suspects ou d'adresses e-mail inconnues.

---
[Source](https://www.bleepingcomputer.com/news/security/simplehelp-bug-lets-hackers-create-rogue-remote-support-accounts/){:target="_blank"}
