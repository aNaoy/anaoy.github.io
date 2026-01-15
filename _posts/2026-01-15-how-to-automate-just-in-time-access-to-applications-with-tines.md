---
title: 'How to automate just-in-time access to applications with Tines'
date: 2026-01-15
permalink: /posts/2026/01/15/how-to-automate-just-in-time-access-to-applications-with-tines/
tags:
- veille-cyber
- bleepingcomp
---
**Automatisation de l'Accès Temporaire aux Applications**

La gestion des identités et des accès (IAM) est essentielle pour les entreprises, mais les contrôles actuels peinent à suivre la croissance et la complexité des environnements modernes. L'octroi d'un accès temporaire, ou "Just-In-Time" (JIT), aux applications sensibles pose un défi majeur, créant un équilibre délicat entre la productivité et la sécurité. Les processus manuels entraînent des lenteurs, une accumulation des privilèges ("privilege creep") et des difficultés à prouver la conformité lors des audits.

Une solution proposée est un workflow automatisé, le "Grant Temporary Application Access" de Tines. Ce workflow orchestre des outils tels que Jira Software, Okta et Slack pour gérer le cycle de vie complet d'une demande d'accès JIT.

**Points Clés :**

*   **Problème :** La gestion manuelle des accès temporaires conduit à des retards, des risques de sécurité accrus dus à l'oubli de révocation des accès et des difficultés de suivi pour les audits.
*   **Solution :** Automatisation du processus de demande, d'approbation, d'octroi et de révocation des accès temporaires.
*   **Outils Orchestrés :** Tines, Okta, Jira Software, Slack (ou Microsoft Teams).

**Fonctionnement du Workflow :**

1.  **Demande en Libre-Service :** L'utilisateur soumet une demande via une page Tines personnalisable, spécifiant l'application et la durée d'accès.
2.  **Approbation Automatisée :** Le workflow identifie le responsable ou le propriétaire de l'application et lui envoie une notification interactive (via Slack) pour approuver ou refuser.
3.  **Provisionnement Instantané :** Sur approbation, Tines contacte Okta pour ajouter l'utilisateur au groupe approprié, accordant l'accès. Une entrée est également créée dans Jira pour la conformité.
4.  **Expiration Automatique :** Le workflow attend la durée définie.
5.  **Révocation Automatique :** À l'expiration, Tines contacte Okta pour retirer l'utilisateur du groupe, révoquant l'accès. Le ticket Jira est mis à jour et l'utilisateur est notifié.

**Vulnérabilités (Non spécifiées dans l'article, mais le problème qu'il adresse :**

*   **Manque de contrôle temporel des accès :** Les accès accordés manuellement peuvent rester actifs indéfiniment, augmentant la surface d'attaque.
*   **Accès excessif ("Privilege Creep") :** Accumulation de droits d'accès non nécessaires au fil du temps.
*   **Complexité de l'audit :** Difficulté à retracer et à prouver la gestion des accès.

**Recommandations :**

*   **Automatiser la gestion des accès temporaires :** Utiliser des plateformes d'orchestration comme Tines pour automatiser l'ensemble du cycle de vie des demandes d'accès JIT.
*   **Mettre en place des revues d'accès régulières :** Bien que l'automatisation de la révocation soit clé, des mécanismes de revue des accès récurrents peuvent compléter la stratégie.
*   **Appliquer le principe du moindre privilège :** Accorder uniquement les accès strictement nécessaires et pour la durée la plus courte possible.
*   **Utiliser des outils intégrés :** Exploiter les intégrations entre les solutions IAM, de gestion de tickets et de communication pour un suivi transparent.
*   **Disposer d'une piste d'audit claire :** Assurer que chaque action d'accès et de révocation est enregistrée de manière centralisée.

Le workflow est disponible dans la bibliothèque Tines et peut être configuré en connectant les outils existants, en personnalisant les formulaires de demande et en ajustant les politiques de sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/how-to-automate-just-in-time-access-to-applications-with-tines/){:target="_blank"}
