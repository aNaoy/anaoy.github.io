---
title: 'Using Gemma4 with Ollama - Testing File Hash Analysis and Recommendations with AI, (Wed, Aug 12th)'
date: 2026-08-13
permalink: /posts/2026/08/13/using-gemma4-with-ollama-testing-file-hash-analysis-and-recommendations-with-ai-wed-aug-12th/
tags:
- veille-cyber
- sans-isc
---
### Analyse et automatisation de la menace par IA : Le cas Gemma 4

Cette étude explore l'utilisation du modèle de langage local **Gemma 4** pour analyser les indicateurs de compromission (IoC) collectés par un capteur **Cowrie** (DShield). L'objectif est d'automatiser l'évaluation des fichiers téléchargés par des attaquants en croisant les données avec des plateformes d'analyse externe (VirusTotal, CyberGordon).

#### Points clés
*   **Comportement malveillant :** Le volume massif de téléchargements récurrents via le capteur Cowrie indique une persistance active, des tentatives d'exfiltration de données et une communication avec des serveurs de commande et contrôle (C2).
*   **Limites des outils :** L'analyse automatique peut échouer si les outils de Threat Intelligence retournent des erreurs de script (ex: "Activer JavaScript"). Une normalisation des flux de données est nécessaire pour une exploitation efficace par l'IA.
*   **Priorisation des sources :** VirusTotal demeure la source primaire recommandée pour l'identification immédiate, tandis que CyberGordon apporte un contexte historique complémentaire.

#### Vulnérabilités (Signatures comportementales)
Bien que les CVE spécifiques ne soient pas listées, les trois hashs principaux identifiés révèlent des vecteurs d'attaque critiques :
1.  `197c7440...` : **Botnet / Loader** (chargement de payloads).
2.  `31d41818...` : **Backdoor / Keylogger** (exfiltration de données/identifiants).
3.  `94f2e4d8...` : **Credential Stealer / Dropper** (installation de composants malveillants).

#### Recommandations pour la sécurisation
*   **Contenir et Isoler :** Considérer tout hôte interagissant avec le capteur comme compromis ; isoler et effectuer une imagerie forensique.
*   **Amélioration du monitoring :** Configurer Cowrie pour surveiller non seulement le téléchargement des fichiers, mais également les tentatives d'exécution.
*   **Filtrage réseau :** Renforcer le filtrage en sortie (egress filtering) et segmenter les réseaux pour limiter les mouvements latéraux.
*   **Chasse aux menaces (Threat Hunting) :** Utiliser les hashs identifiés pour scanner l'ensemble du parc informatique via des solutions EDR afin de détecter une propagation au-delà du capteur.
*   **Optimisation des flux :** Automatiser les requêtes vers les plateformes de renseignement pour garantir une capture complète des résultats et éviter les erreurs de traitement web.

---
[Source](https://isc.sans.edu/diary/rss/33242){:target="_blank"}
