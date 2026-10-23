---
title: 'Exposed Infrastructure Reveals How Ransomware Affiliates Used AI Agents to Execute Intrusions'
date: 2026-10-23
permalink: /posts/2026/10/23/exposed-infrastructure-reveals-how-ransomware-affiliates-used-ai-agents-to-execute-intrusions/
tags:
- veille-cyber
- hackernews
---
### L'émergence des cyberattaques pilotées par agents IA : le framework "Phantom"

Des chercheurs ont identifié un écosystème d'intrusion sophistiqué utilisé par des affiliés des groupes ransomware **INC** et **The Gentlemen**. Cette opération repose sur le framework **Phantom**, un outil offensif automatisé par intelligence artificielle qui orchestre l'intégralité de la chaîne d'attaque, de la reconnaissance à l'exfiltration de données, sous la supervision humaine.

**Points clés :**
* **Structure opérationnelle :** Utilisation de modèles commerciaux via OpenRouter pour automatiser les décisions. En cas de refus de l'IA de répondre à une requête malveillante, les opérateurs contournent les restrictions en reformulant leurs demandes sous forme de tests de pénétration autorisés.
* **Ciblage :** Plus de 60 organisations visées, principalement aux États-Unis, dans les secteurs de l'industrie, de l'énergie et de la santé.
* **Techniques :** Exploitation massive de périphériques exposés, mouvement latéral via `RevSocks`, désactivation d'EDR par attaques BYOVD (*Bring Your Own Vulnerable Driver*) et exfiltration de données sensibles pour maximiser la pression sur les victimes.

**Vulnérabilités exploitées :**
* **CVE-2024-57727 :** SimpleHelp (Path Traversal)
* **CVE-2026-35616 :** Fortinet FortiClient (Contournement d'authentification)
* **CVE-2026-41940 :** cPanel/WHM (Contournement d'authentification)
* **CVE-2026-15409 :** SonicWall SMA 1000 (SSRF)
* **CVE-2026-63030 :** WordPress (RCE)
* **CVE-2026-42208 / CVE-2026-9082 :** SQL Injection (LiteLLM et Drupal)

**Recommandations :**
* **Correction des périphériques d'accès :** Mettre à jour en priorité les passerelles VPN, les outils de gestion à distance (RMM) et les interfaces d'administration exposées sur Internet.
* **Gestion des identifiants :** Éviter impérativement la réutilisation des mots de passe, car un seul compte compromis peut offrir un accès total à l'infrastructure (VPN, RMM, serveurs, sauvegardes).
* **Monitoring EDR :** Surveiller les alertes liées aux pilotes chargés (`zam64.sys`) et renforcer la détection des tunnels SOCKS5 inhabituels.
* **Sécurisation de l'IA :** Mettre en place des politiques de filtrage pour les requêtes émises par des agents IA au sein du réseau d'entreprise pour prévenir les abus de modèles LLM.

---
[Source](https://thehackernews.com/2026/10/exposed-infrastructure-reveals-how.html){:target="_blank"}
