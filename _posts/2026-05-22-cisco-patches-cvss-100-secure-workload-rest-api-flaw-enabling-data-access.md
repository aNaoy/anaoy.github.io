---
title: 'Cisco Patches CVSS 10.0 Secure Workload REST API Flaw Enabling Data Access'
date: 2026-05-22
permalink: /posts/2026/05/22/cisco-patches-cvss-100-secure-workload-rest-api-flaw-enabling-data-access/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans l'API REST de Cisco Secure Workload

Cisco a publié des correctifs pour une faille de sécurité critique affectant **Cisco Secure Workload**, permettant à un attaquant distant non authentifié d'accéder à des données sensibles et de modifier des configurations. Cette vulnérabilité, découverte lors de tests internes, n'a pas encore fait l'objet d'exploitation connue dans la nature.

**Points clés :**
*   **Impact :** Un attaquant peut usurper les privilèges d'un administrateur de site (*Site Admin*) et outrepasser les limites entre les tenants pour lire des informations confidentielles ou modifier les paramètres.
*   **Portée :** La faille concerne les déploiements SaaS et sur site (*on-prem*), indépendamment de la configuration du matériel.
*   **Absence de contournement :** Cisco précise qu'aucune mesure d'atténuation ne permet de contrer cette vulnérabilité en dehors de la mise à jour logicielle.

**Vulnérabilité :**
*   **CVE-2026-20223** (Score CVSS : 10.0) : Défaut de validation et d'authentification insuffisante au niveau des points de terminaison de l'API REST.

**Recommandations :**
Il est impératif de mettre à jour les systèmes vers les versions corrigées dès que possible :
*   Utilisateurs de la version **3.9 ou antérieure** : Migration vers une version corrigée obligatoire.
*   Utilisateurs de la version **3.10** : Mise à jour vers la version **3.10.8.3**.
*   Utilisateurs de la version **4.0** : Mise à jour vers la version **4.0.3.17**.

---
[Source](https://thehackernews.com/2026/05/cisco-patches-cvss-100-secure-workload.html){:target="_blank"}
