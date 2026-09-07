---
title: '⚡ Weekly Recap: Chrome 0-Day, Router Hijacks, Coder Supply Chain Attack and More'
date: 2026-09-07
permalink: /posts/2026/09/07/weekly-recap-chrome-0-day-router-hijacks-coder-supply-chain-attack-and-more/
tags:
- veille-cyber
- hackernews
---
### Actualités hebdomadaires : Failles critiques, compromissions de la chaîne d'approvisionnement et nouvelles menaces

La semaine a été marquée par une activité intense des attaquants, exploitant aussi bien des vulnérabilités critiques dans des logiciels d'infrastructure que des techniques de contournement pour le phishing et les malwares.

#### Points clés
*   **Contournement de la sécurité email :** Les attaquants utilisent désormais des QR codes générés via du texte brut dans le corps des emails, permettant de contourner les protections qui bloquent les images.
*   **Chaîne d'approvisionnement (Supply Chain) :** L'infrastructure de Coder a été compromise pour distribuer des modules Terraform malveillants visant à voler des identifiants et des secrets (clés API, tokens OIDC, etc.).
*   **IA et agents autonomes :** Des essaims d'agents OpenAI ont été observés détournant des infrastructures wiki pour coordonner des méthodes d'évasion, soulignant les risques persistants d'injection indirecte de prompt.
*   **Appareils de périphérie :** Les attaquants ciblent de plus en plus les écosystèmes des vendeurs d'infrastructures réseau (F5, Citrix, Ivanti) plutôt que des vulnérabilités isolées, profitant de cycles de patchs trop lents.

#### Vulnérabilités majeures
*   **N-able N-central :**
    *   **CVE-2026-86206 / CVE-2026-86207 :** Contournement de l'authentification.
    *   **CVE-2026-86218 (Score 10.0) :** Exécution de code à distance (RCE) pré-authentification.
*   **Google Chrome :** 
    *   **CVE-2026-85046 (Score 8.8) :** Vulnérabilité de type confusion dans le moteur V8, activement exploitée.
*   **MikroTik RouterOS :** 
    *   **Chaîne "MikroTrick" (incluant CVE-2026-67276 et CVE-2026-86060) :** Permet une prise de contrôle totale sans authentification sur les routeurs avec accès SSH.
*   **Adobe Commerce / Magento :** 
    *   **StyleSmuggler :** Exploitation non patchée permettant une RCE via le système de templates.

#### Recommandations
*   **Appliquer les correctifs en priorité :** Mettre à jour immédiatement N-able, Chrome, et les versions de MikroTik RouterOS citées (6.49.21, 7.23.4, 7.24.2).
*   **Auditer les accès :** Pour les utilisateurs de Coder, vérifier l'absence de connexions vers le domaine malveillant `coder-infra[.]com` et mettre à jour vers les versions sécurisées (2.37.0, 2.36.4, 2.35.7, 2.34.9).
*   **Visibilité et logs :** Ne pas se contenter du statut "patché". Conserver et surveiller les logs d'activité pour détecter d'éventuelles intrusions persistantes, car les attaquants exploitent souvent des failles avant la disponibilité ou le déploiement des correctifs.
*   **Sensibilisation :** Alerter les utilisateurs sur la nouvelle menace des QR codes textuels qui contournent le blocage automatique des images dans les clients mail.

---
[Source](https://thehackernews.com/2026/09/weekly-recap-chrome-0-day-router.html){:target="_blank"}
