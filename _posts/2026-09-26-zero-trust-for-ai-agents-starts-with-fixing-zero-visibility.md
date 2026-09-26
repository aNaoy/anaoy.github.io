---
title: 'Zero Trust for AI Agents Starts With Fixing Zero Visibility'
date: 2026-09-26
permalink: /posts/2026/09/26/zero-trust-for-ai-agents-starts-with-fixing-zero-visibility/
tags:
- veille-cyber
- hackernews
---
### La visibilité avant tout : Le pilier du Zero Trust pour les agents IA

L'essor rapide des agents IA dans les organisations crée une crise de « Shadow AI » où une grande majorité des flux de données autonomes échappe au contrôle de l'informatique. La mise en œuvre d'une architecture Zero Trust est vouée à l'échec si elle ne repose pas sur une visibilité totale du parc. Avant toute politique de filtrage ou d'autorisation, l'inventaire des agents doit être la priorité absolue.

#### Points clés
*   **Crise de l'inventaire :** 70 % des organisations utilisent des workflows IA sans supervision complète. Un agent sans propriétaire ni périmètre défini ne peut être sécurisé.
*   **Limites de la surveillance traditionnelle :** Le chiffrement TLS et la diversité des environnements (navigateur, endpoint, SaaS) rendent la détection réseau insuffisante.
*   **Instabilité de l'audit :** Les audits ponctuels sont inefficaces face à la nature éphémère des agents IA, capables de générer des clones temporaires pour exfiltrer des données.
*   **Identité spécifique :** Un agent ne doit pas hériter des privilèges de son utilisateur. Chaque agent doit disposer de sa propre identité et de permissions liées exclusivement à sa tâche.

#### Défis et vulnérabilités
*   **Shadow IT :** Déploiement non autorisé d'agents sur des infrastructures personnelles (ex: cas METR), contournant les contrôles de sécurité et les limites de coûts API.
*   **Blind Spots (Angles morts) :** Les outils de sécurité classiques (EDR/NDR) ne voient pas l'IA intégrée aux navigateurs ou aux extensions SaaS.
*   **Attaques par clones éphémères :** Utilisation d'agents à durée de vie très courte pour échapper à la détection par logs ou audits périodiques.

#### Recommandations
1.  **Prioriser la découverte (Know first, then restrict) :** Avant de bloquer, établir un inventaire en utilisant les données de facturation (Cloud/API), les logs de proxy de sortie, les données DNS/SNI et les empreintes (JA4).
2.  **Corréler les sources :** Centraliser les signaux provenant de multiples vecteurs (logs SaaS, jetons OAuth, télémétrie endpoint et logs de navigation) pour reconstruire le comportement des agents.
3.  **Moderniser la journalisation :** Enregistrer les appels d'outils et les actions réelles effectuées par l'agent, et non plus seulement les prompts.
4.  **Implémenter des identités distinctes :** Isoler chaque agent avec un accès limité et spécifique à sa fonction.
5.  **Passer au monitoring continu :** Privilégier une surveillance automatisée capable de détecter des anomalies en temps réel, tout en conservant une responsabilité humaine pour la gouvernance.

---
[Source](https://thehackernews.com/2026/09/zero-trust-for-ai-agents-starts-with.html){:target="_blank"}
