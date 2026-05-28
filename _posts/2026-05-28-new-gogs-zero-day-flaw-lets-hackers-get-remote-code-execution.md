---
title: 'New Gogs zero-day flaw lets hackers get remote code execution'
date: 2026-05-28
permalink: /posts/2026/05/28/new-gogs-zero-day-flaw-lets-hackers-get-remote-code-execution/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique d'exécution de code à distance (RCE) dans Gogs

Une vulnérabilité de type "zero-day" affectant le service Git auto-hébergé **Gogs** permet à un attaquant authentifié d'exécuter du code à distance (RCE) sur le serveur. Bien qu'aucun identifiant CVE ne soit encore attribué, cette faille critique touche les versions 0.14.2 et 0.15.0+dev.

**Points clés :**
*   **Vecteur d'attaque :** Injection d'arguments via une manipulation des noms de branches lors d'une opération de fusion (*rebase*).
*   **Exploitation facilitée :** La configuration par défaut de Gogs autorise l'inscription libre (`DISABLE_REGISTRATION = false`) et la création illimitée de dépôts, permettant à n'importe quel attaquant de créer un compte et d'exploiter la faille sans droits administrateur.
*   **Impact :** Compromission totale du serveur, accès aux dépôts privés, récupération d'identifiants (clés SSH, tokens API, secrets 2FA), et possibilité de mouvement latéral dans le réseau.
*   **Contexte :** Plus de 2 400 instances exposées sont recensées mondialement, principalement en Asie et en Europe. Les mainteneurs de Gogs ont été informés en mars mais n'ont pas encore fourni de correctif.

**Vulnérabilités mentionnées :**
*   **Zero-day actuelle :** Injection d'arguments dans la fonction `Merge()` (non patchée).
*   **Antécédents :** CVE-2025-8110 (RCE précédemment exploitée), CVE-2024-39933, CVE-2024-39932, CVE-2026-26194, CVE-2024-39930.

**Recommandations :**
*   **Désactiver l'inscription publique :** S'assurer que `DISABLE_REGISTRATION` est défini sur `true` dans la configuration pour empêcher la création de comptes anonymes.
*   **Isolation :** Limiter l'exposition des instances Gogs sur Internet (utilisation d'un VPN ou restriction IP).
*   **Surveillance :** Surveiller étroitement les logs du serveur à la recherche d'activités suspectes liées aux opérations de fusion.
*   **Veille :** Surveiller les publications officielles de Gogs pour l'application d'un correctif dès sa disponibilité.

---
[Source](https://www.bleepingcomputer.com/news/security/new-gogs-zero-day-flaw-lets-hackers-get-remote-code-execution/){:target="_blank"}
