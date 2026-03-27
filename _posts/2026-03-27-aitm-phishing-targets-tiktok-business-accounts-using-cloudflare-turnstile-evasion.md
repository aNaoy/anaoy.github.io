---
title: 'AitM Phishing Targets TikTok Business Accounts Using Cloudflare Turnstile Evasion'
date: 2026-03-27
permalink: /posts/2026/03/27/aitm-phishing-targets-tiktok-business-accounts-using-cloudflare-turnstile-evasion/
tags:
- veille-cyber
- hackernews
---
### Campagne de phishing AitM ciblant les comptes TikTok Business

Une nouvelle campagne de phishing par adversaire au milieu (AitM) cible activement les comptes "TikTok for Business". Les attaquants utilisent des pages frauduleuses imitant TikTok ou Google Careers pour dérober des identifiants. Pour contourner la sécurité, les assaillants intègrent une vérification Cloudflare Turnstile, empêchant les outils d'analyse automatisés de détecter la nature malveillante des pages.

**Points clés :**
*   **Objectif :** Vol de comptes professionnels pour diffuser de la malvertising ou des malwares (type Vidar, StealC, Aura Stealer).
*   **Technique :** Utilisation de l'ingénierie sociale (promesses d'opportunités professionnelles) redirigeant vers des pages AitM.
*   **Contournement :** Emploi de Cloudflare Turnstile pour protéger les serveurs de phishing contre l'analyse par des scanners de sécurité.
*   **Vecteur secondaire :** Une campagne distincte utilise des fichiers SVG malveillants pour distribuer des ransomwares (BianLian) via des redirections abusant de raccourcisseurs d'URL (ja.cat).

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car la menace repose sur l'exploitation de l'ingénierie sociale et le détournement de services légitimes (Cloudflare Turnstile, services de raccourcissement d'URL).

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à la méfiance envers les emails non sollicités proposant des opportunités d'emploi ou des liens de connexion.
*   **Authentification :** Implémenter l'authentification multifacteur (MFA) résistante au phishing (clés de sécurité FIDO2/WebAuthn), seule protection efficace contre les attaques AitM.
*   **Filtrage :** Renforcer les politiques de filtrage des emails pour bloquer les domaines récemment créés liés à "career" et limiter l'exécution de pièces jointes inhabituelles (fichiers SVG).
*   **Surveillance :** Surveiller les accès aux comptes professionnels et révoquer immédiatement les sessions suspectes.

---
[Source](https://thehackernews.com/2026/03/aitm-phishing-targets-tiktok-business.html){:target="_blank"}
