---
title: 'Microsoft says backend change broke Teams Free chat and calls'
date: 2026-04-29
permalink: /posts/2026/04/29/microsoft-says-backend-change-broke-teams-free-chat-and-calls/
tags:
- veille-cyber
- bleepingcomp
---
### Incident technique : Dysfonctionnement de Microsoft Teams Free

Une modification récente de l'infrastructure backend de Microsoft a engendré une dégradation du service pour les utilisateurs de la version gratuite de Teams. Ce problème, signalé pour la première fois le 8 avril, empêche certains nouveaux utilisateurs d'accéder aux fonctionnalités de messagerie et d'appels.

**Points clés :**
*   **Cause racine :** Une mise à jour backend a provoqué le contournement automatique des écrans d'onboarding et de consentement à la confidentialité lors de l'inscription.
*   **Impact :** Les profils affectés sont incomplets, ce qui rend les utilisateurs « invisibles » ou « inconnus » dans l'annuaire, empêchant toute interaction (recherche, chat ou appel).
*   **Nature du problème :** Microsoft qualifie cet incident de « dégradation de service » plutôt que de panne totale.

**Vulnérabilités :**
*   Aucune CVE n'a été attribuée, car il s'agit d'un bug de logique métier lié à une mise à jour de service et non d'une faille de sécurité exploitable.

**Recommandations :**
*   **Pour les utilisateurs :** Aucun correctif manuel n'est actuellement disponible. Il est conseillé de surveiller le tableau de bord de santé des services Microsoft (Service Health Status) pour les mises à jour.
*   **Pour les administrateurs :** Bien que le problème concerne la version « Free », il est recommandé de suivre l'évolution des correctifs de service déployés par Microsoft, qui multiplie actuellement les incidents de stabilité sur ses clients Teams (notamment suite à des mises à jour Edge ou des déploiements backend).

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-says-backend-change-broke-teams-free-chat-and-calls/){:target="_blank"}
