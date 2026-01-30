---
title: 'SmarterMail Fixes Critical Unauthenticated RCE Flaw with CVSS 9.3 Score'
date: 2026-01-30
permalink: /posts/2026/01/30/smartermail-fixes-critical-unauthenticated-rce-flaw-with-cvss-93-score/
tags:
- veille-cyber
- hackernews
---
**Mise à jour de SmarterMail pour corriger des failles critiques**

SmarterTools a corrigé plusieurs failles de sécurité dans son logiciel de messagerie SmarterMail, dont une vulnérabilité critique permettant l'exécution de code à distance sans authentification.

**Points clés :**

*   Une vulnérabilité critique (CVE-2026-24423) avec un score CVSS de 9.3 a été corrigée. Elle permettait à un attaquant d'exécuter des commandes sur le système d'exploitation via le ConnectToHub API.
*   Une autre faille critique (CVE-2026-23760), également notée 9.3, qui était activement exploitée, a été corrigée dans le même build.
*   Une vulnérabilité de gravité moyenne (CVE-2026-25067, CVSS 6.9) a été corrigée. Elle permettait des attaques par relais NTLM et une authentification réseau non autorisée en raison d'une mauvaise gestion des chemins de fichiers.

**Vulnérabilités identifiées :**

*   **CVE-2026-24423** : Exécution de code à distance non authentifiée via l'API ConnectToHub.
*   **CVE-2026-23760** : (Détails non fournis dans l'extrait, mais notée comme critique et activement exploitée).
*   **CVE-2026-25067** : Mauvaise gestion des chemins d'accès non authentifiée permettant des attaques par relais NTLM et une authentification réseau non autorisée.

**Recommandations :**

*   Mettre à jour SmarterMail vers le build 9511 (pour CVE-2026-24423 et CVE-2026-23760) ou le build 9518 (pour CVE-2026-25067).
*   Il est fortement recommandé aux utilisateurs de procéder à cette mise à jour dès que possible, compte tenu de l'exploitation active de certaines de ces failles.

---
[Source](https://thehackernews.com/2026/01/smartermail-fixes-critical.html){:target="_blank"}
