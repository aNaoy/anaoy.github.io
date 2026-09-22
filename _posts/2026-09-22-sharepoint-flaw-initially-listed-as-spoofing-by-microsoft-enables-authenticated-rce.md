---
title: 'SharePoint Flaw Initially Listed as Spoofing by Microsoft Enables Authenticated RCE'
date: 2026-09-22
permalink: /posts/2026/09/22/sharepoint-flaw-initially-listed-as-spoofing-by-microsoft-enables-authenticated-rce/
tags:
- veille-cyber
- hackernews
---
### Escalade de privilèges : La vulnérabilité SharePoint sous-estimée

Une vulnérabilité critique dans Microsoft SharePoint Server, initialement classée à tort par l'éditeur comme un simple problème d'usurpation (spoofing), permet en réalité une exécution de code à distance (RCE) authentifiée.

**Points clés :**
* **Gravité sous-évaluée :** Microsoft a d'abord attribué un score CVSS de 6,5 à la faille avant qu'une analyse plus poussée par le chercheur Dinh Ho Anh Khoa ne révèle sa nature réelle, élevant le score à 8,8.
* **Mécanisme de l'attaque :** La faille réside dans le composant `ToolPane` de SharePoint, qui traite mal les directives de balisage. En injectant des quotes non échappées, un attaquant peut contourner les listes de contrôle de sécurité (`SafeControls`) et charger des classes .NET arbitraires.
* **Impact :** Une fois le contrôle chargé, l'attaquant peut déclencher une exécution de code via la désérialisation, permettant le déploiement d'un webshell en mémoire.
* **Chaînage :** La vulnérabilité peut être combinée avec un contournement d'authentification (corrigé en juin 2025) pour permettre une exécution de code à distance sans authentification préalable sur les serveurs autorisant l'accès anonyme.

**Vulnérabilité identifiée :**
* **CVE-2026-65660** : Affecte SharePoint Server 2016, 2019 et Subscription Edition (ainsi que la version 2013, désormais hors support).

**Recommandations :**
* **Appliquer les correctifs :** Installez les mises à jour de sécurité disponibles depuis le 11 août 2025. Le correctif désactive par défaut la fonction vulnérable.
* **Audit de sécurité :** Vérifiez que les serveurs SharePoint ont bien reçu les correctifs de juin et août 2025 pour prévenir toute tentative d'exploitation, y compris les scénarios pré-authentification.

---
[Source](https://thehackernews.com/2026/09/sharepoint-flaw-initially-listed-as.html){:target="_blank"}
