---
title: 'SolarWinds warns of critical Web Help Desk RCE, auth bypass flaws'
date: 2026-01-28
permalink: /posts/2026/01/28/solarwinds-warns-of-critical-web-help-desk-rce-auth-bypass-flaws/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour de sécurité critique pour SolarWinds Web Help Desk

SolarWinds a publié des correctifs pour des vulnérabilités critiques dans son logiciel Web Help Desk (WHD). Ces failles permettent à des acteurs malveillants, même sans authentification, d'exécuter des commandes à distance et de contourner l'authentification.

**Points Clés :**

*   Des mises à jour ont été déployées pour corriger plusieurs failles de sécurité majeures.
*   Le logiciel Web Help Desk est largement utilisé par de grandes organisations, y compris des entités gouvernementales et du secteur de la santé.
*   Ce produit a déjà été la cible d'exploitations passées.

**Vulnérabilités corrigées :**

*   **CVE-2025-40552 et CVE-2025-40554 :** Vulnérabilités de contournement d'authentification permettant à des attaquants non authentifiés d'exploiter le système avec des attaques de faible complexité.
*   **CVE-2025-40553 :** Vulnérabilité critique d'exécution de code à distance (RCE) due à une désérialisation de données non fiable, permettant l'exécution de commandes sur des hôtes vulnérables par des attaquants sans privilèges.
*   **CVE-2025-40551 :** Autre vulnérabilité RCE, découverte par Horizon3.ai, qui permet également à des attaquants non authentifiés d'exécuter des commandes à distance.
*   **CVE-2025-40537 :** Vulnérabilité de haute gravité liée à des identifiants codés en dur, pouvant accorder à des acteurs disposant de privilèges faibles un accès non autorisé aux fonctions administratives.

**Recommandations :**

*   Appliquer immédiatement les mises à jour vers la version Web Help Desk 2026.1.
*   Les administrateurs sont fortement conseillés de mettre à jour leurs systèmes dès que possible en raison de la fréquence d'exploitation des vulnérabilités WHD dans le passé.

---
[Source](https://www.bleepingcomputer.com/news/security/solarwinds-warns-of-critical-web-help-desk-rce-auth-bypass-flaws/){:target="_blank"}
