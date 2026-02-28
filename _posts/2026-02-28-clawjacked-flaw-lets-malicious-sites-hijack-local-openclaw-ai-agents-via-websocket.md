---
title: 'ClawJacked Flaw Lets Malicious Sites Hijack Local OpenClaw AI Agents via WebSocket'
date: 2026-02-28
permalink: /posts/2026/02/28/clawjacked-flaw-lets-malicious-sites-hijack-local-openclaw-ai-agents-via-websocket/
tags:
- veille-cyber
- hackernews
---
### Sécurité d'OpenClaw : Exploitation et Vulnérabilités

Une faille critique dans OpenClaw, baptisée "ClawJacked", permettait à des sites web malveillants de prendre le contrôle des agents d'intelligence artificielle locaux. Cette vulnérabilité, présente dans le cœur du système, autorisait un script malveillant à se connecter au port du passerelle OpenClaw sur `localhost`, puis à contourner le mot de passe via une attaque par force brute, faute de limitation de débit. Une fois authentifié avec des permissions d'administrateur, le script enregistrait discrètement un nouvel appareil, approuvé automatiquement par la passerelle sans intervention de l'utilisateur, accordant ainsi un contrôle total sur l'agent IA. Ce contrôle permettait l'interaction, l'extraction de données de configuration, l'énumération des nœuds connectés et la lecture des journaux d'application.

OpenClaw a corrigé cette vulnérabilité dans la version 2026.2.25. Les utilisateurs sont fortement encouragés à mettre à jour leur logiciel et à auditer régulièrement les accès accordés aux agents IA.

Outre la faille ClawJacked, plusieurs autres vulnérabilités ont été identifiées et corrigées dans différentes versions d'OpenClaw :

*   **Vulnérabilités générales (versions 2026.1.20, 2026.1.29, 2026.2.1, 2026.2.2, 2026.2.14)** : Des failles de sécurité allant de sévérité modérée à élevée, incluant l'exécution de code à distance, l'injection de commandes, la falsification de requêtes côté serveur (SSRF), le contournement d'authentification et le parcours de répertoires. Des identifiants CVE associés incluent CVE-2026-25593, CVE-2026-24763, CVE-2026-25157, CVE-2026-25475, CVE-2026-26319, CVE-2026-26322, CVE-2026-26329.

*   **Vulnérabilité de "poison de logs" (version 2026.2.13)** : Permettait aux attaquants d'écrire du contenu malveillant dans les fichiers journaux via des requêtes WebSocket. Cela pouvait mener à des injections de prompt indirectes, manipulant le raisonnement de l'agent, influençant les étapes de dépannage, et potentiellement divulguer des données ou utiliser des intégrations de manière abusive.

De plus, l'écosystème de ClawHub, le marché ouvert pour les compétences OpenClaw, est devenu une cible pour la distribution de logiciels malveillants. Des compétences malveillantes déguisées en outils légitimes ont été utilisées pour distribuer une nouvelle variante d'Atomic Stealer, un voleur d'informations pour macOS. D'autres attaques observées exploitent des commentaires sur des pages de compétences légitimes pour inciter les utilisateurs à exécuter des commandes malveillantes, ou encore, créent des chaînes d'attaque agent-à-agent pour des escroqueries aux cryptomonnaies.

**Points Clés :**

*   Une faille critique (ClawJacked) permettait à des sites web malveillants de contrôler les agents IA locaux OpenClaw via WebSocket.
*   L'exploitation impliquait un accès au passerelle OpenClaw sur `localhost`, un contournement du mot de passe et une approbation automatique de nouveaux appareils.
*   Plusieurs autres vulnérabilités ont été corrigées, affectant l'exécution de code, les injections, l'authentification et le parcours de répertoires.
*   Le marché de compétences ClawHub est utilisé pour distribuer des logiciels malveillants, y compris des voleurs d'informations et des escroqueries aux cryptomonnaies.
*   Microsoft a émis un avis soulignant les risques de déploiement non gardé d'OpenClaw, recommandant son exécution dans des environnements isolés avec des identifiants non privilégiés.

**Vulnérabilités Identifiées (avec CVE si disponibles) :**

*   ClawJacked (faille critique, pas de CVE mentionné dans l'article)
*   Exécution de code à distance, injection de commandes, SSRF, contournement d'authentification, parcours de répertoires : CVE-2026-25593, CVE-2026-24763, CVE-2026-25157, CVE-2026-25475, CVE-2026-26319, CVE-2026-26322, CVE-2026-26329.
*   Poison de logs (pas de CVE mentionné dans l'article)

**Recommandations :**

*   Mettre à jour OpenClaw vers les dernières versions corrigées (notamment 2026.2.25 pour ClawJacked et 2026.2.13 pour le poison de logs).
*   Auditer régulièrement les accès accordés aux agents IA.
*   Appliquer des contrôles de gouvernance appropriés pour les identités d'agents.
*   Auditer méticuleusement les compétences avant de les installer depuis ClawHub.
*   Éviter de fournir des identifiants et des clés sauf nécessité absolue.
*   Surveiller le comportement des compétences installées.
*   Traiter OpenClaw comme un environnement d'exécution de code non fiable avec des identifiants persistants.
*   Pour les organisations, déployer OpenClaw uniquement dans un environnement entièrement isolé (VM dédiée ou système physique séparé) avec des identifiants dédiés et non privilégiés, n'accédant qu'à des données non sensibles.
*   Mettre en place une surveillance continue et un plan de reconstruction.

---
[Source](https://thehackernews.com/2026/02/clawjacked-flaw-lets-malicious-sites.html){:target="_blank"}
