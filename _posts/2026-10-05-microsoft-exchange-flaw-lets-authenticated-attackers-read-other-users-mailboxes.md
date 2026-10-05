---
title: 'Microsoft Exchange Flaw Lets Authenticated Attackers Read Other Users Mailboxes'
date: 2026-10-05
permalink: /posts/2026/10/05/microsoft-exchange-flaw-lets-authenticated-attackers-read-other-users-mailboxes/
tags:
- veille-cyber
- hackernews
---
### Risque d'accès non autorisé aux boîtes mail sur Microsoft Exchange

Microsoft a publié des correctifs urgents pour une vulnérabilité critique affectant ses serveurs Exchange, permettant à un utilisateur authentifié d'élever ses privilèges au sein d'une organisation.

**Points clés :**
*   **Impact :** Un attaquant authentifié peut accéder aux boîtes de réception, aux messages et aux pièces jointes d'autres utilisateurs au sein de la même entité.
*   **Portée :** L'attaque est limitée à une même organisation (pas d'accès entre différents locataires).
*   **Urgence :** Bien qu'aucune exploitation active ne soit constatée, Microsoft qualifie la probabilité d'exploitation de « plus probable », rendant le déploiement des correctifs impératif.

**Vulnérabilité :**
*   **CVE-2026-96940 :** Vulnérabilité de type « autorisation faible » (CVSS : 8.8).

**Produits impactés :**
*   Microsoft Exchange Server Subscription Edition RTM.
*   Microsoft Exchange Server 2016 (CU23).
*   Microsoft Exchange Server 2019 (CU14 et CU15).

**Recommandations :**
*   **Exchange Online :** Aucune action requise, le correctif a été déployé côté serveur par Microsoft.
*   **Serveurs On-Premise :** Installer immédiatement les mises à jour de sécurité fournies par Microsoft pour les versions listées ci-dessus.

---
[Source](https://thehackernews.com/2026/10/microsoft-exchange-flaw-lets.html){:target="_blank"}
