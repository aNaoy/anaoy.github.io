---
title: 'New Java-Based QuimaRAT MaaS Built to Run on Windows, Linux, and macOS'
date: 2026-07-06
permalink: /posts/2026/07/06/new-java-based-quimarat-maas-built-to-run-on-windows-linux-and-macos/
tags:
- veille-cyber
- hackernews
---
### QuimaRAT : Une nouvelle plateforme de malware multiplateforme en mode service

QuimaRAT est un cheval de Troie d'accès à distance (RAT) sophistiqué, basé sur Java, proposé sous un modèle de « Malware-as-a-Service » (MaaS). Développé pour cibler Windows, Linux et macOS, ce logiciel malveillant se distingue par son architecture modulaire et ses capacités avancées d'évasion.

**Points clés :**
*   **Modèle commercial :** Vendu par abonnement (de 150 $ par mois à 1 200 $ à vie).
*   **Écosystème complet :** Le kit comprend le RAT (Quima Control), un générateur de payloads (Quima Builder), un service de livraison par cache de navigateur (Quima Loader) et un générateur de fichiers HTML/SVG (Quima Dropper).
*   **Architecture technique :** Utilise Java et Apache Maven avec des bibliothèques natives (JNA) pour interagir avec les API bas niveau des systèmes d'exploitation.
*   **Persistance et furtivité :** Utilise des techniques natives (clés de registre, tâches planifiées, dossiers de démarrage, LaunchAgents, crontab) et intègre des mécanismes pour contourner les protections de type Windows SmartScreen.
*   **C2 dynamique :** Le serveur de commande et contrôle peut être mis à jour via Pastebin, permettant aux attaquants de modifier l'infrastructure sans redéployer le malware.

**Vulnérabilités et vecteurs d'attaque :**
Bien qu'aucune CVE spécifique ne soit exploitée, le malware utilise des tactiques de détournement de confiance :
*   **Ingénierie sociale :** Utilisation de pages de leurre (fausses mises à jour ou captchas) pour inciter les victimes à télécharger des « loaders » légitimes qui exécutent ensuite la charge utile en mémoire.
*   **Abus de fonctionnalités natives :** Le malware exploite des outils système pré-approuvés par Windows pour éviter la détection par les antivirus.

**Recommandations de sécurité :**
*   **Surveillance des points de terminaison :** Inspecter régulièrement les clés de registre de persistance, les tâches planifiées (Windows), les entrées `.desktop`/`crontab` (Linux) et les `LaunchAgents` (macOS).
*   **Contrôle des privilèges :** Restreindre les autorisations administratives des utilisateurs, particulièrement sur macOS où certaines fonctionnalités intrusives (capture d'écran, contrôle d'entrée) nécessitent des permissions explicites.
*   **Filtrage Web et E-mail :** Mettre en œuvre une sécurité stricte sur la navigation web pour bloquer les tentatives de livraison via cache de navigateur et sensibiliser les utilisateurs contre les faux messages de mise à jour ou de sécurité.
*   **Analyse comportementale :** Privilégier des solutions EDR capables de détecter des comportements anormaux (exécution de processus multiples, connexions sortantes suspectes vers des C2) plutôt que de se baser uniquement sur la détection de signatures statiques.

---
[Source](https://thehackernews.com/2026/07/new-java-based-quimarat-maas-built-to.html){:target="_blank"}
