---
title: 'AWS Kiro Flaw Let a Poisoned Web Page Rewrite Its Config and Run Code'
date: 2026-07-21
permalink: /posts/2026/07/21/aws-kiro-flaw-let-a-poisoned-web-page-rewrite-its-config-and-run-code/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans l'IDE agentique AWS Kiro

Une faille de sécurité majeure dans l'IDE agentique AWS Kiro permettait à un attaquant d'exécuter du code arbitraire sur la machine d'un développeur via une simple injection de prompt par page web.

**Points clés :**
*   **Mécanisme d'attaque :** L'IDE Kiro possède la capacité de lire des pages web. En insérant du texte invisible (police 1px) dans une documentation technique, un attaquant pouvait forcer l'agent à modifier son propre fichier de configuration (`mcp.json`).
*   **Contournement :** Bien que Kiro demande parfois une approbation pour les changements de configuration, la faille permettait à l'agent de recharger automatiquement le fichier malveillant sans réelle validation de la part de l'utilisateur.
*   **Impact :** L'exécution de code avec les privilèges du développeur permettait le vol de données (identifiants, code source) ou l'installation de persistance.
*   **Contexte :** Ce problème de conception récurrent, où l'agent peut modifier ses propres fichiers de configuration d'exécution, a été identifié à plusieurs reprises depuis 2025.

**Vulnérabilités associées :**
*   Pas de CVE attribuée pour cette découverte spécifique.
*   *Note :* Une faille similaire (auto-exécution via `tasks.json`) a été référencée sous **CVE-2026-10591**.

**Recommandations :**
*   **Mise à jour immédiate :** Les utilisateurs doivent impérativement passer à la version **1.0.x** (ou au minimum la version **0.11.130**), qui intègre un modèle de permissions basé sur des chemins protégés.
*   **Sécurisation au niveau de la plateforme :** AWS a modifié l'architecture de Kiro pour que les fichiers sensibles (config, dossiers .git, etc.) soient protégés par une validation système indépendante de l'IA, empêchant ainsi l'agent de se compromettre lui-même.
*   **Prudence :** Ne pas considérer le "mode supervisé" comme une barrière de sécurité absolue ; les agents IA ne doivent pas avoir la main libre sur les fichiers de configuration système de leur propre environnement.

---
[Source](https://thehackernews.com/2026/07/aws-kiro-flaw-let-poisoned-web-page.html){:target="_blank"}
