---
title: 'Google Chrome adds new security layer for Gemini AI agentic browsing'
date: 2025-12-08
permalink: /posts/2025/12/08/google-chrome-adds-new-security-layer-for-gemini-ai-agentic-browsing/
tags:
- veille-cyber
- bleepingcomp
---
**Chrome Renforce la Sécurité de la Navigation par IA avec Gemini**

Google intègre une nouvelle couche de sécurité au sein de son navigateur Chrome pour protéger les futures fonctionnalités de navigation autonome par IA, basées sur Gemini. Ces fonctionnalités permettent à un agent IA d'accomplir des tâches complexes sur le web de manière autonome.

La principale nouveauté est le "User Alignment Critic", un modèle d'IA distinct, isolé du contenu potentiellement non fiable. Ce composant agit comme un système de haute confiance, vérifiant chaque action envisagée par l'agent IA principal. Il examine les métadonnées et évalue la sécurité de l'action. Si une action est jugée risquée ou non pertinente par rapport à l'objectif défini par l'utilisateur, le système propose une nouvelle tentative ou redonne le contrôle à l'utilisateur.

**Points Clés :**

*   **Navigation Agentique par IA :** Des agents IA autonomes effectuant des tâches multi-étapes sur le web.
*   **User Alignment Critic :** Un modèle d'IA secondaire et isolé pour valider les actions de l'agent principal.
*   **Protection contre l'injection de prompt indirecte :** La nouvelle architecture vise à empêcher que du contenu malveillant sur une page web ne manipule les agents IA pour des actions dangereuses.
*   **Approche multicouche :** Combinaison de règles déterministes, de protections au niveau du modèle, d'isolations et de supervision utilisateur.
*   **Tests continus :** Google utilise des systèmes de "red teaming" automatisés pour tester et améliorer constamment les défenses.

**Vulnérabilités Ciblées :**

L'architecture vise à prévenir les risques liés à :

*   **Injection de prompt indirecte :** Manipulation des agents IA via le contenu web. (Pas de CVE spécifique mentionné dans l'article).
*   **Fuite de données inter-sites :** Empêcher le transfert non autorisé de données entre différents sites web.
*   **Transactions frauduleuses :** Bloquer les actions menant à des transactions illicites.
*   **Compromission d'identifiants :** Protéger la fuite de mots de passe ou d'autres informations sensibles.

**Recommandations et Mesures de Sécurité :**

*   **User Alignment Critic :** Un modèle d'IA isolé pour auditer et valider les actions des agents IA.
*   **Origin Sets :** Restriction de l'accès de l'agent aux sites web spécifiques et aux éléments pertinents, empêchant les interactions avec des origines non approuvées (comme les iframes non autorisées).
*   **Supervision utilisateur :** Demande de confirmation manuelle par l'utilisateur pour les actions sur des sites sensibles (banques, gestionnaires de mots de passe).
*   **Détection d'injection de prompt :** Un classifieur dédié analyse les pages pour détecter les tentatives d'injection de prompt.
*   **Mises à jour automatiques :** Les correctifs de sécurité sont déployés rapidement via le mécanisme de mise à jour automatique de Chrome.
*   **Programme de Bug Bounty :** Google propose des récompenses allant jusqu'à 20 000 $ pour ceux qui parviennent à compromettre le nouveau système, encourageant ainsi la recherche de vulnérabilités.

---
[Source](https://www.bleepingcomputer.com/news/security/google-chrome-adds-new-security-layer-for-gemini-ai-agentic-browsing/){:target="_blank"}
