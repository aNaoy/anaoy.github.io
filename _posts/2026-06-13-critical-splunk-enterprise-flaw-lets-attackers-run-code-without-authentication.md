---
title: 'Critical Splunk Enterprise Flaw Lets Attackers Run Code Without Authentication'
date: 2026-06-13
permalink: /posts/2026/06/13/critical-splunk-enterprise-flaw-lets-attackers-run-code-without-authentication/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code à distance dans Splunk Enterprise

Splunk a publié des correctifs pour une faille de sécurité critique permettant à un attaquant non authentifié d'effectuer des opérations sur des fichiers et d'exécuter du code arbitraire à distance (RCE) sur les instances Splunk Enterprise.

**Points clés :**
*   La vulnérabilité réside dans le service *sidecar* PostgreSQL de Splunk, qui manque de contrôles d'authentification.
*   En exploitant les endpoints `/v1/postgres/recovery/backup` et `/v1/postgres/recovery/restore`, un attaquant peut restaurer une base de données malveillante.
*   L'attaque permet d'écrire des fichiers arbitraires sur le système de fichiers de Splunk (notamment via la fonction `lo_export` de PostgreSQL), menant à une exécution de code par l'écrasement de scripts Python système.
*   Splunk Cloud n'est pas affecté par cette vulnérabilité.

**Vulnérabilité identifiée :**
*   **CVE-2026-20253** (Score CVSS : 9.8)

**Recommandations :**
*   **Mise à jour immédiate :** Les administrateurs doivent mettre à jour leurs instances vers les versions corrigées :
    *   Splunk Enterprise 10.0.0 – 10.0.6 → vers **10.0.7**
    *   Splunk Enterprise 10.2.0 – 10.2.3 → vers **10.2.4**
*   Splunk Enterprise 10.4 n'est pas concerné par cette faille.

---
[Source](https://thehackernews.com/2026/06/critical-splunk-enterprise-flaw-lets.html){:target="_blank"}
