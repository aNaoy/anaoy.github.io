---
title: 'New NadMesh Botnet Hunts Exposed AI Services for Cloud Keys and Kubernetes Tokens'
date: 2026-07-17
permalink: /posts/2026/07/17/new-nadmesh-botnet-hunts-exposed-ai-services-for-cloud-keys-and-kubernetes-tokens/
tags:
- veille-cyber
- hackernews
---
### NadMesh : Le nouveau botnet ciblant les services IA et les accès Cloud

Le botnet **NadMesh** (écrit en Go) s'est propagé rapidement depuis début juillet, ciblant spécifiquement les services d'intelligence artificielle (IA) et de gestion de flux mal protégés pour dérober des identifiants sensibles. Contrairement aux botnets classiques cherchant à exploiter des ressources GPU, NadMesh se concentre sur l'exfiltration de clés AWS, de jetons Kubernetes et de configurations Docker afin d'accéder aux infrastructures cloud sous-jacentes.

**Points clés :**
*   **Cibles privilégiées :** Services d'IA tels que ComfyUI, Ollama, n8n, Open WebUI, Langflow et Gradio.
*   ** Vecteur MCP :** Le botnet exploite notamment le protocole *Model Context Protocol* (MCP) via la commande `execute_command`, profitant du fait que l'authentification reste souvent optionnelle dans ces déploiements.
*   **Persistance :** L'agent utilise des techniques d'obfuscation avancées (Garble, UPX) et une persistance multiple pour résister aux tentatives de suppression.
*   **Stratégie de balayage :** Le botnet utilise un système dynamique qui privilégie les sous-réseaux ayant déjà donné des résultats positifs et ignore les cibles suspectées d'être des "honeypots".

**Vulnérabilités exploitées :**
*   **CVE-2026-39987 :** RCE pré-authentification dans les notebooks Marimo.
*   **CVE-2026-41176 :** Permet l'accès non authentifié aux serveurs rclone.
*   **CVE-2022-22947 :** Spring Cloud Gateway (si exposé).
*   **CVE-2017-12611 :** Struts Freemarker tag flaw.
*   *Autres :* APIs Docker (port 2375) exposées, consoles Jenkins vulnérables, instances Redis sans authentification, et mots de passe faibles (Telnet/SSH).

**Recommandations :**
*   **Sécurisation immédiate :** Placer tous les services d'IA (particulièrement sur les ports 8188, 11434, 7860, 5678) derrière une authentification forte ou les retirer de l'accès public.
*   **Audit des systèmes :** Vérifier la présence de fichiers suspects dans `/tmp/.a`, `/var/tmp/.a` ou dans les tâches planifiées (`/etc/cron.d/`).
*   **Gestion des accès :** Si une compromission est détectée, isoler l'hôte, révoquer immédiatement toutes les clés AWS et jetons Kubernetes, puis mettre à jour les secrets après avoir supprimé la persistance de l'agent.
*   **Mises à jour :** Appliquer les correctifs de sécurité pour les applications citées (Marimo, rclone, etc.) et fermer les ports administratifs inutiles.

---
[Source](https://thehackernews.com/2026/07/new-nadmesh-botnet-hunts-exposed-ai.html){:target="_blank"}
