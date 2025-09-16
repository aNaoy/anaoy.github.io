---
title: 'Securing the Agentic Era: Introducing Astrixs AI Agent Control Plane'
date: 2025-09-16
permalink: /posts/2025/09/16/securing-the-agentic-era-introducing-astrixs-ai-agent-control-plane/
tags:
- veille-cyber
- hackernews
---
### Sécurisation des Agents IA : Le Plan de Contrôle d'Astrix

L'adoption rapide des agents IA dans les entreprises, avec leur autonomie croissante et leur accès aux systèmes, présente des risques de sécurité significatifs. 80% des organisations ont déjà subi des actions imprévues de la part de ces agents, incluant des accès non autorisés et des fuites de données. Les solutions de gestion des identités et des accès (IAM) traditionnelles ne sont pas adaptées à cette nouvelle réalité, notamment en raison des identités non humaines (NHI) des agents et de leur fonctionnement continu.

Astrix propose un Plan de Contrôle des Agents (ACP) conçu pour sécuriser le déploiement d'agents IA. Cette solution octroie des identifiants temporaires, précisément délimités, et un accès basé sur le principe du moindre privilège, limitant ainsi le chaos d'accès et les risques de conformité.

**Points Clés :**

*   **Visibilité et Auditabilité :** L'ACP centralise la visibilité sur chaque agent, ses permissions et ses actions, simplifiant les audits et la validation.
*   **Accès Sécurisé :** Il garantit un accès limité dans le temps et au juste nécessaire dès le déploiement initial, minimisant les risques.
*   **Productivité des Développeurs :** En fournissant des politiques d'accès pré-approuvées, il accélère le déploiement des agents tout en maintenant la sécurité.

**Fonctionnement :**

1.  **Définition des Politiques :** Les administrateurs créent des profils d'autorisations granulaires basés sur le moindre privilège pour des cas d'usage spécifiques d'agents IA.
2.  **Déploiement des Agents :** Les développeurs déploient les agents en appliquant le profil d'autorisations approprié.
3.  **Contrôle Centralisé :** L'ACP offre un inventaire centralisé des agents, de leurs politiques, permettant une surveillance et une gestion en temps réel.

**Avantages par équipe :**

*   **Sécurité :** Visibilité complète, révocation instantanée, preuves disponibles sur demande.
*   **Développement :** API ou CLI simplifiée pour demander l'accès conforme aux politiques, avec des garde-fous pour maintenir la vélocité.
*   **Direction :** Accélération du déploiement sécurisé, cycles d'audit raccourcis, réduction de la portée des incidents.

Le cadre "Discover–Secure–Deploy" d'Astrix permet de découvrir les agents et leurs identifiants, de sécuriser les privilèges excessifs et les menaces, et de déployer des agents IA en toute confiance avec des politiques de Zero Trust et des identifiants "just-in-time".

**Vulnérabilités et Recommandations :**

Bien que l'article ne détaille pas de vulnérabilités spécifiques avec des identifiants CVE, il met en évidence le risque général lié au manque de contrôle sur les agents IA et leurs identités non humaines (NHI).

La principale recommandation est l'adoption d'une solution dédiée telle que l'ACP d'Astrix pour combler ce "point aveugle" croissant, permettant aux organisations de sécuriser et de déployer des agents IA à grande échelle en toute confiance.

---
[Source](https://thehackernews.com/2025/09/securing-agentic-era-introducing.html){:target="_blank"}
