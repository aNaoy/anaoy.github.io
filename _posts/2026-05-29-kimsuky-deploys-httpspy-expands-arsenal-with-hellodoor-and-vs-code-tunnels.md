---
title: 'Kimsuky Deploys HTTPSpy, Expands Arsenal with HelloDoor and VS Code Tunnels'
date: 2026-05-29
permalink: /posts/2026/05/29/kimsuky-deploys-httpspy-expands-arsenal-with-hellodoor-and-vs-code-tunnels/
tags:
- veille-cyber
- hackernews
---
### Évolution et sophistication des campagnes du groupe Kimsuky

Le groupe nord-coréen Kimsuky intensifie ses opérations contre les secteurs militaires, gouvernementaux et industriels sud-coréens. Leurs techniques, observées début 2026, allient ingénierie sociale avancée et utilisation détournée d'outils légitimes pour accroître leur furtivité.

**Points clés :**
*   **Ingénierie sociale :** Utilisation de fausses pages de mise à jour de logiciels de sécurité (type nProtect, AhnLab) et usurpation de services de visioconférence (Cisco Webex) pour piéger les administrateurs et employés.
*   **Technique "JSONPing" :** Utilisation de requêtes JSONP pour vérifier en temps réel si le malware est correctement exécuté sur la machine de la victime avant de délivrer le payload final.
*   **Détournement d'outils légitimes :** Exploitation de VS Code Tunnels pour le maintien d'accès distant et utilisation du logiciel de monitoring DWAgent pour la post-exploitation, contournant ainsi les communications C2 classiques.
*   **Diversification des malwares :** Le groupe utilise un arsenal varié (HTTPSpy, HelloDoor, HttpMalice, AppleSeed, etc.) dont certains composants, comme HelloDoor, sont écrits en Rust et potentiellement générés via des outils d'IA (LLM).

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais souligne une exploitation massive de la confiance des utilisateurs envers les logiciels de sécurité et les services de collaboration. Le risque réside dans l'exécution de fichiers malveillants masqués par des processus légitimes (`regsvr32.exe`, PowerShell, VS Code).

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à la vigilance concernant les pages de téléchargement de logiciels, même si elles semblent légitimes.
*   **Contrôle des accès :** Restreindre l'utilisation des fonctionnalités de tunneling distant (VS Code Tunnels, DWAgent) via les politiques de groupe ou les solutions EDR.
*   **Surveillance réseau :** Détecter les connexions inhabituelles vers des domaines de type "Cloudflare Quick Tunnels" ou vers des infrastructures C2 suspectes.
*   **Analyse comportementale :** Surveiller les exécutions PowerShell suspectes, le recours à des scripts (JSE, PIF, SCR) et les activités liées aux certificats système (ex: `C:\GPKI`), souvent ciblés par les outils de vol de données.

---
[Source](https://thehackernews.com/2026/05/kimsuky-deploys-httpspy-expands-arsenal.html){:target="_blank"}
