---
title: 'Docker Fixes Critical Two-Year-Old Hub Flaw That Let One User Push Images as Another'
date: 2026-10-13
permalink: /posts/2026/10/13/docker-fixes-critical-two-year-old-hub-flaw-that-let-one-user-push-images-as-another/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "GhostPat" sur Docker Hub : Analyse et remédiation

Docker a corrigé une faille critique présente pendant plus de deux ans sur Docker Hub, permettant à un utilisateur malveillant d'usurper l'identité d'un autre utilisateur pour manipuler des images de conteneurs.

**Points clés :**
*   **Nature de la faille :** Le processus de conversion d'un compte personnel en organisation transférait indûment les jetons d'accès personnels (PAT) vers le nouvel utilisateur désigné comme propriétaire, sans consentement ni notification.
*   **Impact :** Un attaquant pouvait utiliser les jetons transférés pour extraire, pousser ou supprimer des images au nom de la victime au sein du registre.
*   **Portée :** La faille ne permettait pas de prendre le contrôle total du compte (pas d'accès au mot de passe ou aux paramètres 2FA).
*   **État actuel :** Docker a déployé un correctif côté serveur le 30 septembre 2026. Aucune preuve d'exploitation malveillante n'a été constatée après examen des logs.

**Vulnérabilité :**
*   **Identifiant :** CVE-2026-105445
*   **Score CVSS :** 9.4 (Critique)

**Recommandations :**
1.  **Vérification des jetons :** Inspectez vos paramètres de compte sous "Personal access tokens" pour identifier des jetons suspects (créations inconnues ou dates incohérentes) et révoquez-les si nécessaire.
2.  **Gestion des accès :** Pour les environnements d'organisation, privilégiez l'utilisation des "Organization access tokens" (disponibles pour les abonnements Docker Team ou Business) au lieu des jetons personnels (PAT).
3.  **Audits de logs :** Les propriétaires d'organisations éligibles doivent consulter régulièrement les journaux d'activité (Activity Logs) pour détecter toute poussée (push) d'image non autorisée.
4.  **Rotation de sécurité :** Par mesure de précaution, il est conseillé de renouveler régulièrement les jetons d'accès utilisés pour l'automatisation CI/CD.

---
[Source](https://thehackernews.com/2026/10/docker-fixes-critical-two-year-old-hub.html){:target="_blank"}
