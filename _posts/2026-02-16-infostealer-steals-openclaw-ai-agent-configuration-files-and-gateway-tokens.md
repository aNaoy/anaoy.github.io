---
title: 'Infostealer Steals OpenClaw AI Agent Configuration Files and Gateway Tokens'
date: 2026-02-16
permalink: /posts/2026/02/16/infostealer-steals-openclaw-ai-agent-configuration-files-and-gateway-tokens/
tags:
- veille-cyber
- hackernews
---
### Alerte de sécurité : Vol de données sensibles et vulnérabilités dans l'écosystème OpenClaw

Des chercheurs en cybersécurité ont identifié une nouvelle menace : un logiciel malveillant (infostealer) capable d'exfiltrer des fichiers de configuration et des jetons d'authentification d'agents d'intelligence artificielle OpenClaw. Cette évolution marque un passage de la simple capture d'identifiants de navigateur à l'exploitation des données critiques des agents IA personnels. Le logiciel malveillant en question serait une variante de Vidar, un infostealer connu depuis fin 2018. Il opère via une routine de collecte de fichiers généraliste, ciblant des extensions et répertoires spécifiques contenant des informations sensibles.

Les fichiers ciblés incluent :
*   `openclaw.json`: contient le jeton du passerelle OpenClaw, l'adresse e-mail de la victime et le chemin de son espace de travail.
*   `device.json`: contient les clés cryptographiques pour les opérations de couplage et de signature au sein d'OpenClaw.
*   `soul.md`: contient les principes opérationnels, les directives comportementales et les limites éthiques de l'agent.

Le vol du jeton d'authentification du passerelle pourrait permettre à un attaquant de se connecter à distance à l'instance OpenClaw de la victime, si le port est exposé, ou d'usurper son identité dans des requêtes vers le passerelle IA.

**Points clés :**

*   **Évolution des menaces :** Les infostealers ciblent désormais les données des agents IA personnels, comme OpenClaw.
*   **Méthode d'attaque :** Extraction de fichiers de configuration via une routine de recherche générique, et non un module spécifique à OpenClaw.
*   **Risques accrus :** Le vol de jetons d'authentification ouvre la voie à un accès non autorisé et à l'usurpation d'identité.
*   **Attaques de la chaîne d'approvisionnement :** Des campagnes malveillantes sur ClawHub utilisent désormais des sites web OpenClaw contrefaits pour contourner les détections.
*   **Vulnérabilités multiples :** Des problèmes tels que l'impossibilité de supprimer des comptes sur Moltbook (un forum pour agents IA) et des centaines de milliers d'instances OpenClaw exposées ont été signalés.

**Vulnérabilités identifiées :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article pour le logiciel malveillant lui-même.
*   Des vulnérabilités de type **Remote Code Execution (RCE)** sont suspectées sur des instances OpenClaw exposées, permettant à un attaquant d'exécuter du code arbitraire sur le système sous-jacent. Ces vulnérabilités peuvent servir de point de pivot pour des attaques plus vastes si l'instance OpenClaw dispose de permissions étendues (e-mails, APIs, services cloud, etc.).
*   Le problème de **non-suppression des comptes sur Moltbook** représente un risque pour la vie privée des utilisateurs.

**Recommandations :**

Bien que l'article ne fournisse pas de liste exhaustive de recommandations directes pour les utilisateurs, il met en évidence des mesures prises par les mainteneurs d'OpenClaw et des bonnes pratiques implicites :

*   **Pour les utilisateurs d'OpenClaw :**
    *   Être vigilant quant à l'exposition des instances OpenClaw et aux permissions accordées.
    *   Examiner attentivement les compétences et les sources avant de les utiliser sur ClawHub.
    *   Se tenir informé des mises à jour de sécurité concernant OpenClaw et les plateformes associées.
    *   Sécuriser les fichiers de configuration et les jetons d'authentification, comme on le ferait pour d'autres identifiants sensibles.
*   **Pour les développeurs et mainteneurs d'OpenClaw :**
    *   Continuer le partenariat avec VirusTotal pour scanner les compétences malveillantes.
    *   Établir un modèle de menace robuste pour anticiper les attaques.
    *   Implémenter des mécanismes de vérification pour les configurations potentiellement erronées (audit pour misconfigurations).
    *   Renforcer la sécurité pour prévenir les vulnérabilités RCE et les problèmes de gestion des comptes.

---
[Source](https://thehackernews.com/2026/02/infostealer-steals-openclaw-ai-agent.html){:target="_blank"}
