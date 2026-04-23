---
title: 'Vercel Finds More Compromised Accounts in Context.ai-Linked Breach'
date: 2026-04-23
permalink: /posts/2026/04/23/vercel-finds-more-compromised-accounts-in-contextai-linked-breach/
tags:
- veille-cyber
- hackernews
---
### Extension de la compromission des comptes Vercel via un incident lié à l'IA

Vercel a identifié de nouveaux comptes clients compromis à la suite d'une enquête approfondie sur son infrastructure. Cette brèche trouve son origine dans l'utilisation par un employé d'un outil tiers, **Context.ai**, dont les accès ont été détournés suite à une infection par le logiciel malveillant **Lumma Stealer**.

**Points clés :**
* **Propagation de la brèche :** Les attaquants ont compromis un employé de Context.ai, accédé à son compte Google Workspace, puis pivoté vers son compte Vercel pour infiltrer les systèmes internes et décrypter des variables d'environnement.
* **Shadow AI :** L'incident souligne les risques liés au « Shadow AI », où l'utilisation d'outils d'IA non approuvés par le service informatique permet à des attaquants de contourner les protocoles de sécurité classiques via des intégrations OAuth.
* **Incidents multiples :** En dehors de cette intrusion, Vercel a découvert d'autres comptes compromis indépendamment, potentiellement via du phishing ou des malwares classiques.

**Vulnérabilités :**
* **Infection par infostealer :** Utilisation de **Lumma Stealer** (ciblant les identifiants et tokens de session).
* **Détournement d'OAuth :** Exploitation de la confiance héritée des intégrations tierces pour masquer les activités malveillantes.
* **Absence de CVE spécifique :** La faille repose ici sur des vecteurs d'attaque humains et comportementaux (social engineering, logiciels non autorisés) plutôt que sur une vulnérabilité logicielle isolée.

**Recommandations :**
* **Gestion du Shadow AI :** Interdire ou soumettre à un audit de sécurité strict l'utilisation de tout outil d'IA tiers au sein de l'entreprise.
* **Surveillance des intégrations :** Réévaluer régulièrement les permissions accordées aux applications tierces via OAuth.
* **Gestion des accès et des variables :** Sécuriser davantage les variables d'environnement sensibles et renforcer la surveillance des journaux d'accès pour détecter rapidement les comportements anormaux (énumération).
* **Sensibilisation :** Renforcer la formation des employés contre le téléchargement de logiciels douteux (scripts de jeu, cracks) favorisant l'installation d'infostealers.

---
[Source](https://thehackernews.com/2026/04/vercel-finds-more-compromised-accounts.html){:target="_blank"}
