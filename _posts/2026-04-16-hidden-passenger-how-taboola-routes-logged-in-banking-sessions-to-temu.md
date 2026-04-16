---
title: 'Hidden Passenger? How Taboola Routes Logged-In Banking Sessions to Temu'
date: 2026-04-16
permalink: /posts/2026/04/16/hidden-passenger-how-taboola-routes-logged-in-banking-sessions-to-temu/
tags:
- veille-cyber
- hackernews
---
### Shadow Tracking : Le danger des redirections invisibles par les pixels tiers

Des chercheurs ont découvert qu'un pixel publicitaire légitime, intégré par une institution bancaire, redirigeait silencieusement les sessions authentifiées des utilisateurs vers les serveurs de suivi de Temu. Ce mécanisme, opérant via une redirection HTTP 302, permet à des tiers de collecter des données sur le comportement des utilisateurs au sein d'environnements bancaires sécurisés, sans que les outils de sécurité traditionnels ne détectent l'anomalie.

**Points clés :**
*   **Biais du premier saut :** La majorité des outils de sécurité (WAF, CSP, analyse statique) valident uniquement le domaine initial du script, ignorant les destinations finales après redirection.
*   **Fuite de données :** L'utilisation de l'en-tête `Access-Control-Allow-Credentials: true` force le navigateur à inclure des cookies lors de la redirection vers le domaine tiers, permettant une corrélation entre la session bancaire et un profil publicitaire.
*   **Impact réglementaire :** Ce procédé constitue une violation majeure du RGPD (absence de consentement, transfert illégal de données) et contrevient aux normes de sécurité PCI DSS (exigence 6.4.3).

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'un **détournement de fonctionnalité légitime** (abus de confiance dans la chaîne de requêtes) plutôt que d'une faille logicielle classique.

**Recommandations :**
*   **Surveillance du runtime :** Ne plus se limiter aux listes blanches de domaines déclarés ; inspecter le comportement réel des scripts au moment de l'exécution dans le navigateur.
*   **Audit des tiers :** Soumettre les scripts marketing et publicitaires au même niveau de rigueur sécuritaire et juridique que les intégrations backend critiques.
*   **Politique de sécurité :** Renforcer la politique de sécurité du contenu (CSP) pour limiter les redirections non autorisées et auditer régulièrement les chaînes de requêtes complexes initiées par des partenaires tiers.

---
[Source](https://thehackernews.com/2026/04/hidden-passenger-how-taboola-routes.html){:target="_blank"}
