---
title: 'Varonis Atlas: Securing AI and the Data That Powers It'
date: 2026-03-23
permalink: /posts/2026/03/23/varonis-atlas-securing-ai-and-the-data-that-powers-it/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation intégrale de l'IA avec Varonis Atlas

Varonis Atlas est une plateforme de sécurité de bout en bout conçue pour découvrir, protéger et gouverner les systèmes d'IA en entreprise. Elle se distingue en intégrant le contexte de la donnée à la sécurité de l'IA, permettant une surveillance continue des agents, des LLM et des infrastructures d'IA.

**Points clés :**
* **Visibilité totale :** Découverte automatisée des systèmes d'IA (sanctionnés ou « Shadow AI ») et cartographie de leurs accès aux données.
* **Posture de sécurité (AI-SPM) :** Évaluation continue des vulnérabilités, des mauvaises configurations et des risques liés aux agents.
* **Protection en temps réel :** Utilisation d'une passerelle d'IA (AI Gateway) pour inspecter les requêtes, bloquer les comportements malveillants et prévenir les fuites de données sensibles.
* **Test et gouvernance :** Tests d'intrusion automatisés et conformité aux cadres réglementaires (EU AI Act, NIST AI RMF).
* **Surveillance et réponse :** Détection des menaces spécifiques à l'IA (injections de prompts, jailbreaks) avec intégration aux outils SIEM/SOAR.

**Vulnérabilités adressées :**
* *Note : L'article ne mentionne pas de CVE spécifiques, car il se concentre sur les vecteurs de menaces structurelles de l'IA.*
* **Risques identifiés :** Injection de prompts, jailbreaks, contournement de politiques de sécurité, fuite de données confidentielles via les agents, et accès aux données trop permissifs (« Over-privileged access »).

**Recommandations :**
* **Inventaire continu :** Identifier l'ensemble des agents et outils IA utilisés au sein de l'organisation pour éliminer le « Shadow AI ».
* **Approche axée sur les données :** Ne pas se limiter à la sécurité du modèle, mais lier chaque action de l'IA à la sensibilité des données qu'elle manipule.
* **Test dynamique :** Effectuer des tests d'intrusion réguliers en production contre les terminaux LLM.
* **Guardrails en ligne :** Déployer des contrôles de sécurité dans le flux des requêtes pour bloquer les comportements non conformes avant qu'ils ne s'exécutent.

---
[Source](https://www.bleepingcomputer.com/news/security/varonis-atlas-securing-ai-and-the-data-that-powers-it/){:target="_blank"}
