---
title: 'New Attacks Trick OpenClaw AI Agent Into Running Code and Leaking Secrets'
date: 2026-06-11
permalink: /posts/2026/06/11/new-attacks-trick-openclaw-ai-agent-into-running-code-and-leaking-secrets/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités et risques de sécurité dans l'agent IA OpenClaw

Des recherches récentes menées par Imperva et Varonis ont mis en évidence des failles critiques dans l'agent IA OpenClaw, permettant à des attaquants de détourner son fonctionnement pour exécuter du code arbitraire ou exfiltrer des données sensibles.

**Points clés :**
*   **Injection par objet de message :** L'agent traite de manière indifférenciée les données provenant d'objets (contacts partagés, vCards, localisations) et les instructions système. Des charges utiles injectées dans ces objets peuvent être exécutées par le modèle sans que l'utilisateur ne les remarque.
*   **Phishing par agent :** L'agent est vulnérable aux tactiques d'ingénierie sociale. Sa volonté d'être utile et d'accomplir des tâches (ex: export de données, accès à des identifiants) l'amène à ignorer les règles de sécurité face à une demande urgente ou routinière.
*   **Défaut de gestion des identités :** Cinq vulnérabilités liées aux extensions (Slack, Discord, Matrix, Zalo, Teams) permettaient à un attaquant de se faire passer pour un utilisateur autorisé en usurpant son nom d'affichage.
*   **Risque structurel :** Le problème repose sur le "triple létal" : accès à des données privées, traitement de contenu non fiable et capacité à exfiltrer des informations.

**Vulnérabilités :**
*   **CVE non mentionnées :** Bien que des correctifs aient été publiés, les vulnérabilités liées à l'injection par objet de message (corrigée en v2026.4.23) et les erreurs d'identification dans les extensions (corrigées) soulignent des failles de conception persistantes.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **2026.4.23** ou supérieure pour corriger la gestion des métadonnées non fiables.
*   **Renforcement de l'architecture :**
    *   **Contrôle de sortie :** Imposer une validation humaine pour tout envoi d'e-mail vers de nouvelles adresses.
    *   **Segmentation des accès :** Restreindre les permissions des connecteurs selon la source de la tâche (ne pas autoriser un agent traitant des e-mails externes à lire tout un CRM).
    *   **Validation des actions critiques :** Exiger une approbation humaine explicite pour le transfert d'identifiants ou de fonds.
*   **Politique stricte :** Traiter les fichiers d'instruction de l'agent comme une politique de sécurité immuable, et non comme de simples suggestions, en limitant les privilèges au strict nécessaire pour un "employé junior" automatisé.

---
[Source](https://thehackernews.com/2026/06/new-attacks-trick-openclaw-ai-agent.html){:target="_blank"}
