---
title: 'Docker Hub flaw let attackers impersonate users, tamper with images'
date: 2026-10-13
permalink: /posts/2026/10/13/docker-hub-flaw-let-attackers-impersonate-users-tamper-with-images/
tags:
- veille-cyber
- bleepingcomp
---
### Faille critique dans Docker Hub : usurpation d'identité via les jetons PAT

Une vulnérabilité critique a été identifiée dans Docker Hub, permettant à des attaquants d'usurper l'identité d'utilisateurs et de manipuler leurs dépôts de conteneurs. Le problème résidait dans le processus de conversion d'un compte personnel en organisation, qui réattribuait automatiquement les jetons d'accès personnel (PAT) existants au nouveau propriétaire sans révocation ni consentement préalable.

**Points clés :**
*   **Vulnérabilité (CVE-2026-105445) :** Réattribution non sécurisée des jetons PAT lors du changement de propriétaire d'une organisation.
*   **Impact :** Un attaquant pouvait utiliser un jeton valide pour agir au nom de la victime, permettant de lire, modifier ou supprimer des images conteneurisées au sein des dépôts ciblés.
*   **Risque :** Risque majeur pour la chaîne d'approvisionnement logicielle, permettant la publication d'images frauduleuses sous une identité légitime.
*   **Portée limitée :** L'accès via cette faille ne permettait pas de modifier les mots de passe, les adresses e-mail ou les paramètres d'authentification à deux facteurs.

**Recommandations et mesures prises :**
*   **Correctif appliqué :** Docker a corrigé la faille en supprimant le transfert automatique des PAT et en imposant désormais le consentement explicite de l'utilisateur lors de sa désignation comme propriétaire d'une organisation.
*   **Actions correctives :** Docker a désactivé les jetons transférés le 8 octobre 2026.
*   **Vérification :** Seuls les utilisateurs ayant reçu une notification officielle de Docker sont considérés comme impactés ; aucune action n'est requise pour les autres.

---
[Source](https://www.bleepingcomputer.com/news/security/docker-hub-flaw-let-attackers-impersonate-users-tamper-with-images/){:target="_blank"}
