---
title: 'ARTEX AI, Claude agents used in cyberattacks on South Korean banks'
date: 2026-10-10
permalink: /posts/2026/10/10/artex-ai-claude-agents-used-in-cyberattacks-on-south-korean-banks/
tags:
- veille-cyber
- bleepingcomp
---
### Attaques par IA contre le secteur bancaire sud-coréen

Un cyberattaquant sinophone a ciblé plusieurs institutions financières sud-coréennes majeures (Shinhan Bank, KB Kookmin Bank, Hana Bank), provoquant des pannes de systèmes et le vol de données personnelles et bancaires. L'incident marque un tournant dans l'utilisation malveillante de l'intelligence artificielle pour automatiser les cyberattaques.

**Points clés**
* **Outils utilisés :** L'attaquant a exploité « ARTEX AI », une suite de tests d'intrusion agentique initialement open-source, couplée aux agents « Claude Code ».
* **Infrastructure hybride :** Le système utilisait DeepSeek v4.1-flash comme moteur principal, complété par GLM-5.3 et Grok 4.6 pour les sessions Claude.
* **Erreur opérationnelle :** Une mauvaise configuration des répertoires a permis aux chercheurs de CrowdStrike de découvrir des historiques de sessions, des fichiers de configuration et le CV de l'attaquant, révélant une possible identité (un individu de 26 ans basé à Guangdong, en Chine).
* **Conséquence du projet :** Suite à l'utilisation détournée de son outil, le développeur d'ARTEX AI a retiré le projet de l'accès public, bien que des versions dérivées continuent de circuler.

**Vulnérabilités exploitées**
* **Absence de CVE spécifique :** L'attaque repose sur l'utilisation détournée d'outils de test d'intrusion légitimes (offensifs par nature) plutôt que sur l'exploitation d'une faille logicielle unique.
* **Exposition de données :** Le stockage non sécurisé des fichiers de configuration, logs et sessions (répertoires ouverts) a facilité l'attribution de l'attaque par les chercheurs.

**Recommandations**
* **Surveillance des accès IA :** Renforcer la supervision des requêtes émises par des outils d'automatisation et des agents IA au sein des environnements critiques.
* **Sécurisation des configurations :** Auditer strictement les serveurs de développement et les répertoires de travail pour éviter l'exposition accidentelle de fichiers sensibles (logs de sessions, clés d'API, données personnelles).
* **Détection des comportements anormaux :** Mettre en place des outils de détection capables d'identifier des flux de données inhabituels générés par des agents autonomes, souvent plus rapides et persistants que les scans traditionnels.

---
[Source](https://www.bleepingcomputer.com/news/security/hacker-used-artex-ai-and-claude-agents-to-target-south-korean-banks/){:target="_blank"}
