---
title: 'Thinking Fast and Slow in the SOC: The Case for Combining Autonomous AI with Analyst Copilots'
date: 2026-07-13
permalink: /posts/2026/07/13/thinking-fast-and-slow-in-the-soc-the-case-for-combining-autonomous-ai-with-analyst-copilots/
tags:
- veille-cyber
- hackernews
---
### Optimiser le SOC : L'architecture cognitive homme-machine

Pour améliorer l'efficacité des centres d'opérations de sécurité (SOC), cet article propose d'appliquer la théorie des systèmes cognitifs de Daniel Kahneman (*Système 1* pour la pensée rapide/automatique et *Système 2* pour la pensée lente/délibérée) à l'architecture des outils de cybersécurité.

**Points clés :**
*   **Le déséquilibre actuel :** 98 % des alertes de sécurité sont répétitives et ne nécessitent pas d'intervention humaine, tandis que 2 % requièrent une expertise complexe. Les SOC échouent souvent en surchargeant les analystes (Système 2) de tâches répétitives (Système 1), ce qui mène à l'épuisement et à la négligence de menaces réelles cachées dans les alertes de faible priorité.
*   **Le modèle à deux vitesses :** Une architecture efficace doit automatiser 100 % du triage initial via une IA dédiée à l'investigation forensique (Système 1), et réserver les agents IA "copilotes" (type Claude) uniquement à l'analyse complexe, à la remédiation et au hunting (Système 2).
*   **L'accumulation du savoir :** L'externalisation des investigations (MDR) empêche l'organisation de capitaliser sur son propre historique de données. Pour qu'une IA soit réellement performante, elle doit fonctionner sur une base de connaissances propre à l'entreprise.

**Vulnérabilités opérationnelles :**
*   **Fatigue décisionnelle :** L'épuisement des analystes provoque l'omission de signaux faibles, laissant passer des menaces réelles (environ 54 menaces critiques par an dans un volume de 450 000 alertes).
*   **Utilisation inefficiente de l'IA :** Déployer des modèles LLM coûteux sur l'ensemble des alertes brutes est économiquement non viable et constitue un contresens architectural.

**Recommandations :**
*   **Automatiser le "Système 1" :** Implémenter des outils capables d'analyser, de corréler et de fermer les alertes triviales à vitesse machine, sans interaction humaine.
*   **Dédier le "Système 2" à la haute valeur ajoutée :** Utiliser les agents conversationnels (copilotes) exclusivement sur des dossiers déjà documentés et enrichis par le moteur d'investigation automatique.
*   **Internaliser la donnée :** Garder la gestion des investigations et le contexte organisationnel au sein de l'instance de l'entreprise pour permettre au "Système 2" de bénéficier d'un apprentissage continu et spécifique, rendant ainsi le "Système 1" plus intelligent avec le temps.

---
[Source](https://thehackernews.com/2026/07/thinking-fast-and-slow-in-soc-case-for.html){:target="_blank"}
