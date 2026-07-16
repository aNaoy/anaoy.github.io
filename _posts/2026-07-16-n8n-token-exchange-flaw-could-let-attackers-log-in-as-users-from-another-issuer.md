---
title: 'n8n Token Exchange Flaw Could Let Attackers Log In as Users From Another Issuer'
date: 2026-07-16
permalink: /posts/2026/07/16/n8n-token-exchange-flaw-could-let-attackers-log-in-as-users-from-another-issuer/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'usurpation d'identité sur la plateforme n8n

La plateforme d'automatisation **n8n** présentait une faille critique de liaison d'identité au sein de sa fonctionnalité « Token Exchange ». Cette vulnérabilité permettait à un attaquant de se connecter en tant qu'utilisateur légitime sans nécessiter de mot de passe, en exploitant une mauvaise gestion des jetons JWT (JSON Web Tokens).

**Points clés :**
* **Mécanisme défaillant :** Lorsqu'une instance était configurée pour faire confiance à plusieurs émetteurs de jetons, n8n vérifiait uniquement le champ `sub` (subject) du jeton JWT pour identifier l'utilisateur, ignorant le champ `iss` (issuer).
* **Risque :** Si deux émetteurs différents émettaient des jetons avec un identifiant `sub` identique, le système n8n attribuait l'accès au compte utilisateur correspondant, indépendamment de l'émetteur d'origine.
* **Périmètre restreint :** La faille concerne uniquement les déploiements de type Enterprise utilisant la fonctionnalité « Token Exchange » avec plusieurs émetteurs de confiance configurés.

**Vulnérabilité :**
* **CVE-2026-59208 :** Score CVSS 4.0 de 7.6 (élevé).

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs disponibles dans les versions **2.27.4** ou **2.28.1** (et ultérieures).
* **Mesures d'atténuation temporaires :** Si une mise à jour est impossible, réduire le nombre d'émetteurs de confiance à un seul ou désactiver complètement la fonctionnalité « Token Exchange » via la configuration des variables d'environnement (`N8N_TOKEN_EXCHANGE_TRUSTED_KEYS`).
* **Vigilance :** Le correctif n'étant pas mentionné explicitement dans les notes de version habituelles, il est impératif de se référer aux avis de sécurité officiels (GitHub Advisory) pour vérifier l'état de vulnérabilité de son instance.

---
[Source](https://thehackernews.com/2026/07/n8n-token-exchange-flaw-could-let.html){:target="_blank"}
