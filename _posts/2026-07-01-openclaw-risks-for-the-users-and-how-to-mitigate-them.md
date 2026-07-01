---
title: 'OpenClaw: risks for the users and how to mitigate them'
date: 2026-07-01
permalink: /posts/2026/07/01/openclaw-risks-for-the-users-and-how-to-mitigate-them/
tags:
- veille-cyber
- securelist
---
### Sécurité des agents IA : Les risques liés à l'écosystème OpenClaw

OpenClaw (anciennement Clawdbot/Moltbot) est une plateforme d'agents IA largement adoptée pour automatiser des tâches complexes grâce à des « compétences » (skills) interchangeables. Cependant, sa popularité et sa flexibilité ont attiré des acteurs malveillants, exposant les entreprises à des risques de sécurité majeurs.

**Points clés :**
*   **Architecture à risques :** Les agents OpenClaw nécessitent souvent des accès étendus au système de fichiers et aux jetons d'identification, stockés localement en clair ou via des variables d'environnement.
*   **Attaques par "Skills" :** La facilité de création de ces compétences permet la diffusion massive de codes malveillants, assimilables à des attaques par chaîne d'approvisionnement (supply-chain). Plus de 1 100 comptes malveillants ont été identifiés depuis janvier 2026.
*   **Défis de détection :** La nature textuelle des instructions (langage naturel ou scripts) rend la détection traditionnelle par antivirus complexe. Bien que des solutions comme VirusTotal et SkillSpector soient désormais utilisées pour le filtrage, les comportements malveillants dynamiques persistent.

**Vulnérabilités :**
*   Environ 530 vulnérabilités découvertes en deux ans (référencées dans les CVE depuis février 2026).
*   **Nature des failles :** Problèmes critiques de stockage de données sensibles et octroi de privilèges excessifs aux agents, facilitant le détournement de l'IA ou l'injection de commandes malveillantes.

**Recommandations :**
*   **Isolation :** Isoler l'agent OpenClaw des données critiques et des infrastructures sensibles par une protection en couches.
*   **Analyse proactive :** Utiliser des solutions spécialisées (ex: Kaspersky Scan Engine) pour inspecter et filtrer toutes les compétences entrant dans le périmètre de l'entreprise.
*   **Surveillance réseau :** Exploiter les systèmes de bac à sable (sandboxing) fournis par la plateforme et surveiller étroitement les accès réseau effectués par les agents.
*   **Gouvernance :** Établir une politique stricte sur l'usage de l'IA, interdisant l'utilisation d'outils tiers non approuvés par le département informatique.

---
[Source](https://securelist.com/openclaw-security/120484/){:target="_blank"}
