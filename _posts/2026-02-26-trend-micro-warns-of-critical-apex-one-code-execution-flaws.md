---
title: 'Trend Micro warns of critical Apex One code execution flaws'
date: 2026-02-26
permalink: /posts/2026/02/26/trend-micro-warns-of-critical-apex-one-code-execution-flaws/
tags:
- veille-cyber
- bleepingcomp
---
**Menaces Critiques sur Trend Micro Apex One**

Deux failles de sécurité critiques ont été corrigées par Trend Micro sur sa plateforme de sécurité Endpoint Apex One. Ces vulnérabilités permettent à des attaquants d'exécuter du code à distance sur des systèmes Windows non patchés.

**Points Clés :**

*   **Nature des failles :** Les deux vulnérabilités sont des faiblesses de type "path traversal" au sein de la console de gestion de Trend Micro Apex One.
*   **Impact :** Elles permettent à des attaquants non authentifiés d'exécuter du code malveillant.
*   **Prérequis :** L'exploitation réussie nécessite un accès à la console de gestion Trend Micro Apex One.

**Vulnérabilités :**

*   **CVE-2025-71210 :** Une faiblesse de "path traversal" dans la console de gestion Apex One.
*   **CVE-2025-71211 :** Une autre vulnérabilité de "path traversal" similaire dans la console de gestion, affectant un exécutable différent.

**Recommandations :**

*   **Mise à jour immédiate :** Les clients sont fortement encouragés à mettre à jour leurs systèmes vers les dernières versions disponibles dès que possible.
*   **Sécurisation de la console :** Les utilisateurs dont la console Apex One est exposée publiquement devraient envisager des mesures de mitigation, telles que des restrictions de source d'accès.
*   **Application des correctifs :** Trend Micro a publié le Critical Patch Build 14136 pour corriger ces failles critiques, ainsi que des vulnérabilités de moindre gravité affectant les agents Windows et macOS.

Il est important de noter que Trend Micro a déjà alerté sur plusieurs autres vulnérabilités critique de Apex One exploitées par le passé, soulignant la nécessité d'une vigilance constante et de mises à jour régulières.

---
[Source](https://www.bleepingcomputer.com/news/security/trend-micro-warns-of-critical-apex-one-rce-vulnerabilities/){:target="_blank"}
