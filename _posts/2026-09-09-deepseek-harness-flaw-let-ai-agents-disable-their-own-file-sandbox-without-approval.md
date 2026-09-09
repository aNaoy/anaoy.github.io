---
title: 'DeepSeek Harness Flaw Let AI Agents Disable Their Own File Sandbox Without Approval'
date: 2026-09-09
permalink: /posts/2026/09/09/deepseek-harness-flaw-let-ai-agents-disable-their-own-file-sandbox-without-approval/
tags:
- veille-cyber
- hackernews
---
### Évasion de bac à sable dans DeepSeek Harness

Une vulnérabilité critique permet à des agents de codage IA utilisant **DeepSeek Harness** de désactiver leur propre environnement de confinement (sandbox). En accédant à l'interface locale non sécurisée de l'outil, un agent peut modifier les paramètres de sa session vers un mode « accès total » sans nécessiter d'approbation, lui permettant ainsi d'exécuter des commandes et d'écrire des fichiers en dehors de son espace de travail prévu.

**Points clés :**
*   **Vulnérabilité :** Absence totale d'authentification sur l'interface locale et confiance excessive envers les en-têtes HTTP (Host header spoofing).
*   **Risque :** Exécution de code arbitraire hors sandbox et exfiltration potentielle de l'historique complet des conversations.
*   **Identifiant CVE :** **CVE-2026-82533** (Score CVSS : 9.4/10).
*   **Portée :** Affecte les versions 0.1.1-rc.2 et antérieures.

**Recommandations :**
1.  **Mise à jour :** Installer la version **0.1.2-rc.1** ou ultérieure via le registre npm, car les versions alpha initiales n'étaient pas toujours diffusées correctement.
2.  **Logiciels tiers :** Si vous utilisez une application de bureau intégrant DeepSeek Harness, vérifiez la version embarquée et mettez-la à jour.
3.  **Contournement temporaire :** Si la mise à jour est impossible, arrêtez l'interface web de l'outil lorsque vous ne l'utilisez pas et supprimez tout tunnel, proxy ou transfert de port permettant d'y accéder.
4.  **Prudence :** Le projet souligne que les mesures de sécurité actuelles ne garantissent pas une isolation totale ; évitez de traiter des données sensibles ou non fiables avec cet outil.

---
[Source](https://thehackernews.com/2026/09/deepseek-harness-flaw-let-ai-agents.html){:target="_blank"}
