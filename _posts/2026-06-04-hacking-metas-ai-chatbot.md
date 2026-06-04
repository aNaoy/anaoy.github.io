---
title: 'Hacking Meta’s AI Chatbot'
date: 2026-06-04
permalink: /posts/2026/06/04/hacking-metas-ai-chatbot/
tags:
- veille-cyber
- schneier
---
### La vulnérabilité du chatbot d'assistance de Meta

Des pirates ont exploité une faille dans le chatbot d'assistance de Meta pour pirater des comptes Instagram. En manipulant l'intelligence artificielle, les attaquants parvenaient à détourner les procédures de sécurité pour prendre le contrôle de comptes tiers.

**Points clés :**
*   **Mode opératoire :** Les attaquants utilisaient un VPN pour simuler la localisation de la victime, puis demandaient au chatbot de Meta d'associer une nouvelle adresse e-mail au compte cible.
*   **Détournement de processus :** Le chatbot envoyait un code de vérification à l'e-mail de l'attaquant ; une fois ce code partagé avec le bot, celui-ci autorisait la réinitialisation du mot de passe.
*   **Statut :** Meta a annoncé avoir corrigé cette vulnérabilité spécifique, bien que l'ampleur des comptes compromis reste indéterminée.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, car il s'agit d'une vulnérabilité logique liée à la conception et à la confiance excessive accordée à l'IA pour valider des changements critiques de paramètres de sécurité.

**Recommandations :**
*   **Pour les utilisateurs :** Activer l'authentification à deux facteurs (2FA), de préférence via une application d'authentification plutôt que par e-mail ou SMS.
*   **Pour les développeurs :** Ne pas déléguer les actions sensibles (modification d'e-mail, réinitialisation de mot de passe) à des agents conversationnels basés sur des LLM, ces derniers étant intrinsèquement vulnérables au "prompt injection" et aux manipulations logiques. Les procédures de récupération de compte doivent rester strictement automatisées via des protocoles de sécurité rigides et non conversationnels.

---
[Source](https://www.schneier.com/blog/archives/2026/06/hacking-metas-ai-chatbot.html){:target="_blank"}
