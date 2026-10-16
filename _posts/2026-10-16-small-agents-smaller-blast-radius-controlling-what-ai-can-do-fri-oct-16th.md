---
title: 'Small Agents, Smaller Blast Radius: Controlling What AI Can Do, (Fri, Oct 16th)'
date: 2026-10-16
permalink: /posts/2026/10/16/small-agents-smaller-blast-radius-controlling-what-ai-can-do-fri-oct-16th/
tags:
- veille-cyber
- sans-isc
---
### La persistance des CAPTCHA face aux bots

Cet article du SANS Internet Storm Center souligne l'évolution constante de la lutte entre les systèmes de vérification humaine (CAPTCHA) et les outils automatisés. Si les CAPTCHA restent un outil de défense indispensable pour protéger les services web contre les abus, ils ne constituent plus une barrière infranchissable.

**Points clés :**
*   **Efficacité limitée :** Les bots modernes sont capables de contourner de nombreux tests de type "Je ne suis pas un robot" via des services de résolution par IA ou par des humains (fermes de clics).
*   **Complexité vs Expérience utilisateur :** L'article met en avant le dilemme permanent entre le renforcement de la sécurité (rendre le test plus difficile) et la préservation d'une expérience utilisateur fluide.
*   **Nécessité d'une approche multicouche :** Le recours exclusif aux CAPTCHA est insuffisant ; il doit être complété par d'autres mécanismes de détection de trafic illégitime.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique ne soit citée, l'article souligne une vulnérabilité conceptuelle : le **contournement automatisé des mécanismes d'authentification** (Automated Authentication Bypass). Cela permet aux attaquants de réaliser des attaques par force brute, du credential stuffing ou du spam à grande échelle en simulant un comportement humain.

**Recommandations :**
*   **Diversifier les méthodes de défense :** Ne pas se reposer uniquement sur les CAPTCHA. Utiliser des analyses de comportement (analyse de la souris, empreinte du navigateur, en-têtes HTTP).
*   **Limitation de débit (Rate Limiting) :** Implémenter des restrictions strictes sur le nombre de requêtes par adresse IP ou par utilisateur pour limiter l'impact des bots.
*   **Surveillance active :** Analyser les logs pour identifier des modèles de trafic anormaux qui pourraient indiquer une tentative de contournement des protections en place.
*   **Détection proactive :** Utiliser des solutions de "bot management" capables de distinguer les bots légitimes (indexeurs) des bots malveillants via l'analyse de réputation IP.

---
[Source](https://isc.sans.edu/diary/rss/33430){:target="_blank"}
