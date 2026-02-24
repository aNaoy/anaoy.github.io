---
title: 'Anthropic Says Chinese AI Firms Used 16 Million Claude Queries to Copy Model'
date: 2026-02-24
permalink: /posts/2026/02/24/anthropic-says-chinese-ai-firms-used-16-million-claude-queries-to-copy-model/
tags:
- veille-cyber
- hackernews
---
## Extraction de Modèles d'IA : Une Tactique Sophistiquée

Des entreprises chinoises d'intelligence artificielle ont mené des campagnes à grande échelle pour extraire illicitement les capacités du modèle de langage avancé Claude d'Anthropic. Ces attaques par distillation, visant à améliorer leurs propres modèles, ont impliqué plus de 16 millions d'interactions via environ 24 000 comptes frauduleux. Les trois entreprises identifiées sont DeepSeek, Moonshot AI et MiniMax. Ces pratiques violent les conditions d'utilisation d'Anthropic et les restrictions régionales, car l'utilisation de leurs services est interdite en Chine en raison de risques juridiques, réglementaires et de sécurité.

**Points Clés :**

*   **Attaques par Distillation :** Technique où un modèle moins performant est entraîné à partir des sorties d'un système d'IA plus puissant. L'usage est légitime pour optimiser ses propres modèles, mais illégal lorsqu'il est pratiqué par des concurrents pour acquérir des capacités existantes à moindre coût.
*   **Risques de Sécurité Nationale :** Les modèles issus de distillation illicite peuvent manquer des garde-fous nécessaires, permettant la prolifération de capacités dangereuses sans protections adéquates.
*   **Objectifs Malveillants :** Ces modèles non protégés peuvent être exploités par des gouvernements autoritaires pour des opérations cyber offensives, des campagnes de désinformation et une surveillance de masse.
*   **Méthodologie Sophistiquée :** Les campagnes utilisent des comptes frauduleux, des services de proxy commerciaux et des architectures "hydra cluster" pour masquer le trafic et éviter la détection. Le volume et la structure des requêtes étaient distincts d'une utilisation normale, ciblant spécifiquement les capacités avancées de Claude comme le raisonnement agentique, l'utilisation d'outils et le codage.

**Vulnérabilités/Attaques (sans CVE spécifique mentionné dans l'article) :**

*   **Extraction de Modèle par Distillation :** Exploitation des sorties d'un modèle d'IA propriétaire pour entraîner un nouveau modèle.
*   **Utilisation de Compagnies de Proxy Commerciales :** Services offrant un accès à grande échelle à des modèles d'IA via des réseaux de comptes frauduleux.
*   **Détournement de Comptes :** Création et utilisation de milliers de comptes pour générer un volume important de requêtes destinées à l'extraction de données.

**Recommandations d'Anthropic :**

*   **Développement de Classificateurs et Systèmes d'Empreintes Comportementales :** Pour identifier les schémas suspects d'attaques par distillation dans le trafic API.
*   **Renforcement de la Vérification :** Pour les comptes éducatifs, les programmes de recherche en sécurité et les organisations startups.
*   **Mise en Place de Sauvegardes Renforcées :** Pour réduire l'efficacité des sorties de modèle pour la distillation illicite.

Ces attaques par extraction et distillation de modèles ne représentent généralement pas un risque pour les utilisateurs finaux, mais ciblent spécifiquement les développeurs de modèles et les fournisseurs de services d'IA.

---
[Source](https://thehackernews.com/2026/02/anthropic-says-chinese-ai-firms-used-16.html){:target="_blank"}
