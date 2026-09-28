---
title: 'Carbonato Botnet Compromises Docker Hosts to Deploy Telegram-Controlled Hermes AI Agent'
date: 2026-09-28
permalink: /posts/2026/09/28/carbonato-botnet-compromises-docker-hosts-to-deploy-telegram-controlled-hermes-ai-agent/
tags:
- veille-cyber
- hackernews
---
### Carbonato : Un botnet exploitant l'IA pour automatiser les cyberattaques

Le botnet **Carbonato** cible les daemons Docker exposés sans authentification pour déployer le framework **Hermes Agent**. Une fois installé, cet agent est détourné via un fichier de configuration modifié (persona "GH0ST") pour agir comme un expert en cybersécurité malveillant, piloté par les attaquants via Telegram. Le malware utilise des conteneurs privilégiés pour établir une persistance, exfiltrer des identifiants et scanner les réseaux voisins pour se propager automatiquement.

**Points clés :**
*   **Propagation virale :** Utilisation de scans réseaux toutes les 5 minutes pour identifier et infecter d'autres instances Docker vulnérables.
*   **Contrôle par IA :** Hermes Agent interagit avec des modèles de langage (LLM) pour générer et exécuter dynamiquement des commandes système basées sur les instructions reçues sur Telegram.
*   **Évasion :** Utilisation de tunnels SSH inverses, de scripts de surveillance (watchdog) et de tâches cron pour assurer la persistance et éviter la détection.
*   **Tendance émergente :** Carbonato illustre l'essor des attaques automatisées par IA, où des frameworks comme Hermes, Strix ou Cairn sont combinés pour réaliser des campagnes d'exfiltration ou d'exploitation sans intervention humaine constante.

**Vulnérabilités exploitées :**
*   **Exposition du Docker Daemon :** Le vecteur d'entrée principal est le port **2375** (Docker API) laissé ouvert sans authentification. Aucune CVE spécifique n'est mentionnée, car il s'agit d'une erreur de configuration critique permettant un accès root à l'hôte.

**Recommandations :**
*   **Sécurisation de Docker :** Ne jamais exposer le daemon Docker sur Internet sans authentification TLS mutuelle ou restriction stricte par pare-feu (IP whitelisting).
*   **Gestion des privilèges :** Éviter l'exécution de conteneurs en mode `--privileged` sauf nécessité absolue.
*   **Surveillance réseau :** Détecter les connexions sortantes suspectes vers des services de messagerie (Telegram) ou des serveurs SSH inconnus depuis les hôtes Docker.
*   **Hardening des hôtes :** Auditer régulièrement les tâches planifiées (cron jobs) et les nouveaux services SSH installés sur les machines.

---
[Source](https://thehackernews.com/2026/09/carbonato-botnet-compromises-docker.html){:target="_blank"}
