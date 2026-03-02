---
title: 'ClawJacked attack let malicious websites hijack OpenClaw to steal data'
date: 2026-03-02
permalink: /posts/2026/03/02/clawjacked-attack-let-malicious-websites-hijack-openclaw-to-steal-data/
tags:
- veille-cyber
- bleepingcomp
---
### Caméra Cachée : La Faiblesse des Agents IA Locaux

Une faille de sécurité critique, nommée "ClawJacked", a été découverte dans la plateforme d'IA OpenClaw, permettant à des sites web malveillants de prendre le contrôle d'instances locales sans éveiller les soupçons.

Les chercheurs d'Oasis Security ont identifié que le service passerelle d'OpenClaw, par défaut, se lie à l'adresse locale (localhost) et expose une interface WebSocket. Contrairement aux politiques de sécurité des navigateurs pour d'autres origines, les connexions WebSocket vers localhost ne sont pas bloquées. Un utilisateur visitant un site web compromis peut ainsi, via JavaScript, établir silencieusement une connexion à la passerelle locale et tenter une authentification.

Bien qu'OpenClaw intègre une limitation du nombre de tentatives pour prévenir les attaques par force brute, l'adresse de bouclage (127.0.0.1) en est exclue par défaut. Cette particularité permet à un attaquant de tester des centaines de mots de passe par seconde sans que les tentatives échouées soient limitées ou enregistrées. Une fois le mot de passe découvert, l'attaquant peut enregistrer un appareil de confiance, car la passerelle approuve automatiquement les associations depuis localhost sans intervention de l'utilisateur.

Avec une session authentifiée et des permissions d'administrateur, l'agresseur peut accéder aux identifiants, lister les nœuds connectés, voler des informations sensibles stockées par l'IA, lire les journaux d'application, ou encore demander à l'agent de fouiller dans l'historique des messages. Il peut également exfiltrer des fichiers depuis des appareils connectés ou exécuter des commandes shell arbitraires sur les nœuds associés, conduisant à une compromission totale du poste de travail à partir d'un simple onglet de navigateur.

**Points Clés :**

*   **Vulnérabilité "ClawJacked" :** Permet à des sites web malveillants de détourner OpenClaw.
*   **Attaque par Force Brute Silencieuse :** Exploitation de l'absence de limitation sur les connexions localhost.
*   **Prise de Contrôle Complète :** Accès aux données sensibles, exécution de commandes arbitraires.

**Vulnérabilités :**

*   Aucun identifiant CVE n'est mentionné dans l'article. La vulnérabilité réside dans le comportement par défaut de la passerelle OpenClaw et sa gestion des connexions localhost.

**Recommandations :**

*   **Mise à Jour Immédiate :** Installer la version 2026.2.26 d'OpenClaw ou une version ultérieure.
*   **Vigilance :** Être conscient des risques potentiels liés aux référentiels de compétences OpenClaw (comme ClawHub) qui peuvent être utilisés pour diffuser des malwares.

---
[Source](https://www.bleepingcomputer.com/news/security/clawjacked-attack-let-malicious-websites-hijack-openclaw-to-steal-data/){:target="_blank"}
