---
title: 'April Patch Tuesday Fixes Critical Flaws Across SAP, Adobe, Microsoft, Fortinet, and More'
date: 2026-04-15
permalink: /posts/2026/04/15/april-patch-tuesday-fixes-critical-flaws-across-sap-adobe-microsoft-fortinet-and-more/
tags:
- veille-cyber
- hackernews
---
### Vague de correctifs critiques : Patch Tuesday d'avril

Le Patch Tuesday d'avril marque une mobilisation majeure des éditeurs face à de nombreuses failles critiques, dont certaines font déjà l'objet d'exploitations actives.

**Points clés et vulnérabilités majeures**

*   **SAP :** Une injection SQL critique (CVE-2026-27681, score CVSS 9.9) dans SAP Business Planning/Warehouse permet à un utilisateur peu privilégié d'exécuter des commandes SQL arbitraires, menant à l'extraction ou la destruction de données.
*   **Adobe Acrobat Reader :** Une vulnérabilité d'exécution de code à distance (CVE-2026-34621, score CVSS 8.6) est actuellement exploitée par des attaquants dans la nature.
*   **Adobe ColdFusion :** Cinq failles critiques (dont CVE-2026-27304, score 9.3 et CVE-2026-27306, score 8.4) permettent l'exécution de code, le déni de service et le contournement de fonctionnalités de sécurité.
*   **Fortinet (FortiSandbox) :** Deux vulnérabilités critiques (CVE-2026-39813 et CVE-2026-39808, score CVSS 9.1) permettent le contournement de l'authentification et l'injection de commandes système via des requêtes HTTP forgées.
*   **Microsoft SharePoint :** Une faille de usurpation (CVE-2026-32201, score CVSS 6.5) est activement exploitée, facilitant potentiellement l'accès à des informations sensibles et le déplacement latéral au sein des réseaux.

**Recommandations**

*   **Appliquer les correctifs immédiatement :** La priorité doit être donnée à la mise à jour des produits activement exploités (Adobe Acrobat et Microsoft SharePoint).
*   **Mise à jour des systèmes critiques :** Appliquer sans délai les patchs pour SAP Business Planning/Warehouse, Adobe ColdFusion et Fortinet (versions 4.4.9 et 5.0.6 minimum pour FortiSandbox).
*   **Veille étendue :** Étant donné l'ampleur des publications (incluant Apple, Cisco, VMware, Google, etc.), les administrateurs système doivent vérifier les bulletins de sécurité de l'ensemble de leur parc logiciel pour s'assurer qu'aucune mise à jour critique n'a été manquée.

---
[Source](https://thehackernews.com/2026/04/april-patch-tuesday-fixes-critical.html){:target="_blank"}
