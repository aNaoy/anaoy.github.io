---
title: 'Microsoft December 2025 Patch Tuesday fixes 3 zero-days, 57 flaws'
date: 2025-12-09
permalink: /posts/2025/12/09/microsoft-december-2025-patch-tuesday-fixes-3-zero-days-57-flaws/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour de sécurité Microsoft : Décembre 2025**

Microsoft a publié ses mises à jour de sécurité mensuelles, résolvant 57 vulnérabilités. Parmi celles-ci, trois zéro-jours ont été corrigés : un exploité activement et deux divulgués publiquement.

**Points clés :**

*   **Nombre total de vulnérabilités corrigées :** 57
*   **Catégories de vulnérabilités :** 28 élévations de privilèges, 19 exécutions de code à distance, 4 divulgations d'informations, 3 dénis de service, 2 usurpations d'identité.
*   **Vulnérabilités critiques :** 3

**Vulnérabilités notoires (Zero-days) :**

*   **CVE-2025-62221** : Vulnérabilité d'élévation de privilèges dans le pilote de filtre de fichiers Cloud de Windows. Permet à un attaquant local d'obtenir des privilèges système. Cette faille était activement exploitée.
*   **CVE-2025-64671** : Vulnérabilité d'exécution de code à distance dans GitHub Copilot pour Jetbrains. Elle permet à un attaquant d'exécuter des commandes localement via une injection de prompt cross-site dans des fichiers non fiables ou des serveurs MCP.
*   **CVE-2025-54100** : Vulnérabilité d'exécution de code à distance dans PowerShell. Permet à un attaquant d'exécuter du code via des scripts embarqués dans une page web récupérée avec `Invoke-WebRequest`. Microsoft a ajouté un avertissement et recommandé l'utilisation de `-UseBasicParsing`.

**Recommandations :**

*   **Appliquer immédiatement les mises à jour de sécurité :** Il est crucial d'installer les correctifs de Microsoft pour atténuer les risques associés à ces vulnérabilités, en particulier celles déjà exploitées ou divulguées.
*   **Surveiller les indicateurs de compromission :** Les équipes de sécurité doivent rester vigilantes quant aux signes d'exploitation de ces vulnérabilités dans leurs environnements.
*   **Prudence avec `Invoke-WebRequest` dans PowerShell :** Vérifier l'utilisation de `Invoke-WebRequest` et s'assurer que le paramètre `-UseBasicParsing` est utilisé lorsque cela est approprié pour prévenir l'exécution de code malveillant.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-december-2025-patch-tuesday-fixes-3-zero-days-57-flaws/){:target="_blank"}
