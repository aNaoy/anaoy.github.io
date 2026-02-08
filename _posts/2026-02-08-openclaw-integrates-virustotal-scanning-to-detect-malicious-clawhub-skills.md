---
title: 'OpenClaw Integrates VirusTotal Scanning to Detect Malicious ClawHub Skills'
date: 2026-02-08
permalink: /posts/2026/02/08/openclaw-integrates-virustotal-scanning-to-detect-malicious-clawhub-skills/
tags:
- veille-cyber
- hackernews
---
## Sécurité Renforcée pour l'Écosystème des Agents IA : Intégration de VirusTotal et Vulnérabilités Identifiées

OpenClaw, une plateforme d'agents IA open-source, renforce sa sécurité en intégrant l'analyse de VirusTotal pour scanner les "skills" (compétences) disponibles sur son marché, ClawHub. Cette démarche vise à améliorer la protection de l'écosystème des agents autonomes face à la recrudescence de menaces.

### Points Clés :

*   **Partenariat avec VirusTotal :** OpenClaw utilise désormais la plateforme de VirusTotal pour scanner systématiquement chaque nouvelle compétence publiée sur ClawHub.
*   **Analyse Automatisée :** Chaque skill est analysé via un hachage SHA-256 et, si nécessaire, via VirusTotal Code Insight. Les compétences jugées "bénignes" sont approuvées, les "suspectes" signalées, et les "malveillantes" bloquées.
*   **Surveillance Continue :** Les compétences actives sont réanalysées quotidiennement pour détecter d'éventuelles évolutions malveillantes.
*   **Transparence et Roadmap Sécurité :** OpenClaw s'engage à publier un modèle de menace, une feuille de route de sécurité, un processus de signalement des failles et les résultats d'audits de sécurité.
*   **Contexte des Menaces :** Cette mesure intervient suite à la découverte de centaines de compétences malveillantes sur ClawHub, conçues pour exfiltrer des données, installer des backdoors ou propager des malwares.
*   **Risque accru pour les entreprises :** Le déploiement d'OpenClaw sans validation IT/sécurité crée des risques de "Shadow AI", avec un accès potentiellement élevé aux données et aux réseaux de l'entreprise.
*   **Nature des Agents IA :** Contrairement aux logiciels traditionnels, les agents IA interprètent le langage naturel, complexifiant la détection des intentions malveillantes, notamment via l'injection de prompts.

### Vulnérabilités Identifiées (non exhaustif et sans CVE spécifique mentionné dans l'article) :

*   **Stockage de crédits en clair :** Les identifiants et clés API sont stockés sans chiffrement adéquat.
*   **Utilisation de `eval()` avec des entrées utilisateur :** Risque d'exécution de code arbitraire.
*   **Absence de politique de confidentialité claire et de processus de désinstallation sécurisé :** Des données sensibles peuvent subsister après une tentative de suppression.
*   **Attaques par injection de prompt indirectes :** Permettent à des attaquants d'insérer des commandes cachées dans des documents ou des pages web, conduisant à l'installation de backdoors ou à l'exfiltration de données.
*   **Exfiltration de données via des prompts malveillants :** Des compétences conçues pour extraire des fichiers de configuration sensibles (".env", "creds.json") ou des informations d'identification.
*   **Fuites de crédits dans 7.1% des compétences analysées sur ClawHub.**
*   **Clonage et republiation de compétences malveillantes** avec de légères variations de nom.
*   **Vulnérabilité d'exécution de code à distance (RCE) "en un clic" :** Une visite sur une page malveillante pouvait exposer un token d'authentification et permettre l'exécution de commandes.
*   **Liaison par défaut de la passerelle sur 0.0.0.0:18789 :** Rend l'API complètement accessible sur n'importe quelle interface réseau, avec plus de 30 000 instances exposées sur Internet.
*   **Base de données Supabase mal configurée** sur Moltbook, exposant des clés API et des données privées d'agents.
*   **Exploitation de la plateforme Moltbook** pour amplifier la portée des attaques et diriger les agents vers des threads malveillants contenant des injections de prompt.
*   **Manque de filtrage du contenu non fiable** et de garde-fous contre les injections de prompt.
*   **Mémoires et prompts système modifiables** persistant entre les sessions.
*   **Absence d'approbation utilisateur explicite** avant l'exécution d'appels d'outils.
*   **Accès système par défaut sans sandboxing activé.**
*   **Classification erronée du trafic proxifié** comme trafic local, contournant l'authentification pour certaines instances exposées.

### Recommandations :

*   **Activer le sandboxing basé sur Docker** pour les outils utilisés par OpenClaw.
*   **Mettre en œuvre des protections robustes** contre les attaques par injection de prompt.
*   **Sécuriser la gestion des identifiants et des clés API**, éviter le stockage en clair.
*   **Déployer une politique de confidentialité claire** et un processus de désinstallation sécurisé.
*   **Mettre à jour régulièrement** pour corriger les vulnérabilités connues.
*   **Limiter les privilèges accordés aux agents IA** et aux compétences installées.
*   **Établir des contrôles d'accès stricts** et des frontières d'exécution claires pour les outils autonomes.
*   **Surveiller activement les instances exposées** et les configurations par défaut potentiellement dangereuses.
*   **Ne pas s'appuyer uniquement sur la détection d'antivirus** comme seule ligne de défense contre les malwares déguisés en compétences IA.
*   **Sensibiliser les utilisateurs** aux risques associés à l'installation de compétences provenant de sources non fiables.

---
[Source](https://thehackernews.com/2026/02/openclaw-integrates-virustotal-scanning.html){:target="_blank"}
