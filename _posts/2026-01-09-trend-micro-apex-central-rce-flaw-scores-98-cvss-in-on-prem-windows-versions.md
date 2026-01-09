---
title: 'Trend Micro Apex Central RCE Flaw Scores 9.8 CVSS in On-Prem Windows Versions'
date: 2026-01-09
permalink: /posts/2026/01/09/trend-micro-apex-central-rce-flaw-scores-98-cvss-in-on-prem-windows-versions/
tags:
- veille-cyber
- hackernews
---
**Alertes de Sécurité Critiques pour Trend Micro Apex Central**

Des mises à jour de sécurité ont été publiées pour les versions sur site de Trend Micro Apex Central pour Windows, corrigeant plusieurs vulnérabilités dont une faille critique permettant l'exécution de code à distance.

**Points Clés :**

*   Une vulnérabilité majeure, identifiée sous le nom de **CVE-2025-69258**, a un score CVSS de 9.8/10. Elle permet à un attaquant distant non authentifié de charger une DLL malveillante dans un processus clé.
*   Deux autres vulnérabilités, **CVE-2025-69259** et **CVE-2025-69260**, toutes deux avec un score CVSS de 7.5/10, peuvent entraîner des conditions de déni de service pour les attaquants distants non authentifiés.
*   Ces failles affectent les versions d'Apex Central sur site antérieures au build 7190.
*   L'exploitation de ces vulnérabilités requiert que l'attaquant ait déjà un accès physique ou distant à un point de terminaison vulnérable.

**Vulnérabilités :**

*   **CVE-2025-69258** : Exécution de code à distance (RCE) via une vulnérabilité LoadLibraryEX. Un attaquant peut charger une DLL contrôlée par l'attaquant dans un exécutable critique, permettant l'exécution de code sous le contexte SYSTEM.
*   **CVE-2025-69259** : Déni de service (DoS) via une valeur de retour NULL non vérifiée dans le traitement des messages.
*   **CVE-2025-69260** : Déni de service (DoS) via une lecture hors limites dans le traitement des messages.

**Recommandations :**

*   Appliquer rapidement les correctifs et les mises à jour des solutions de sécurité.
*   Examiner et renforcer les politiques d'accès à distance aux systèmes critiques.
*   S'assurer que la sécurité du périmètre est à jour.

---
[Source](https://thehackernews.com/2026/01/trend-micro-apex-central-rce-flaw.html){:target="_blank"}
