---
title: '⚡ Weekly Recap: Cisco 0-Day, AI Agent RCE, ClickFix Attacks, ClickFix Surge, and Browser Hijacks'
date: 2026-09-21
permalink: /posts/2026/09/21/weekly-recap-cisco-0-day-ai-agent-rce-clickfix-attacks-clickfix-surge-and-browser-hijacks/
tags:
- veille-cyber
- hackernews
---
### Actualités de la semaine : Vulnérabilités critiques et menaces liées à l'IA

Cette semaine a été marquée par une recrudescence d'attaques "ClickFix", des vulnérabilités critiques dans des solutions d'entreprise et des risques accrus liés aux agents IA.

#### **Points clés**
*   **Attaques ClickFix :** Utilisation croissante de leurres de type "réparation manuelle" (via Google Docs, scripts injectés sur des sites tiers ou extensions de navigateur malveillantes) pour inciter les utilisateurs à exécuter des commandes malveillantes.
*   **Risques liés à l'IA :** Découverte de *Plugin4Shell*, une faille permettant une exécution de code à distance (RCE) zéro-clic sur des agents de codage (GitHub Copilot, Gemini CLI, etc.) en contournant la vérification SHA des plugins.
*   **Chaînage de vulnérabilités :** Des chercheurs ont démontré l'utilisation de l'IA (Claude Opus 5) pour automatiser le chaînage de failles critiques et accéder aux référentiels internes d'OpenAI.

#### **Vulnérabilités majeures**
*   **Cisco ISE :** **CVE-2026-76460** (Score 10.0) – Contournement d'authentification via un endpoint API, activement exploité.
*   **Discourse (Forum) :** **CVE-2026-32882** – RCE liée à `libheif` (corrigée en version 1.22.0).
*   **Logiciels divers :** De nombreuses CVE critiques affectant notamment le noyau Linux, les produits Dell, Okta, Chrome, Firefox, et le serveur DNS BIND 9.

#### **Recommandations**
*   **Patching urgent :** Appliquer immédiatement les correctifs pour le **Cisco Identity Services Engine (ISE)**.
*   **Sécurisation des outils IA :** Mettre à jour tous les agents de codage (Copilot, Claude Code, etc.) vers les dernières versions pour contrer le bypass de vérification de plugins.
*   **Sensibilisation ClickFix :** Informer les utilisateurs de ne jamais copier/coller des commandes dans un terminal ou dans une console de navigateur suite à une demande affichée sur une page web ou un document partagé.
*   **Gestion des accès :** Auditer les configurations Cloud et les accès API (notamment pour les outils tiers comme Brevo, suite à l'incident d'API Key).
*   **Veille :** Suivre les recommandations de sécurité pour les composants spécifiques (ex: mises à jour Chrome/Firefox/Bind) listés dans la section CVE de l'article.

---
[Source](https://thehackernews.com/2026/09/weekly-recap-cisco-0-day-ai-agent-rce.html){:target="_blank"}
