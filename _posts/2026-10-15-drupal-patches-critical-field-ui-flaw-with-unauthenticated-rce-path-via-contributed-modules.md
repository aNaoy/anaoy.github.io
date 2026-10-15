---
title: 'Drupal Patches Critical Field UI Flaw With Unauthenticated RCE Path via Contributed Modules'
date: 2026-10-15
permalink: /posts/2026/10/15/drupal-patches-critical-field-ui-flaw-with-unauthenticated-rce-path-via-contributed-modules/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code à distance (RCE) dans Drupal

Une faille critique a été identifiée dans le module « Field UI » de Drupal, permettant à un attaquant d'exécuter du code arbitraire sur le serveur. Bien que cette vulnérabilité ne soit pas exploitable via le cœur de Drupal seul, elle peut être déclenchée par des modules tiers ou du code personnalisé, y compris sans authentification préalable.

**Points clés :**
*   **Vulnérabilité identifiée :** CVE-2026-108097 (Score de risque : 19/25).
*   **Mécanisme :** Le système de rendu exécutait des fonctions de rappel (callbacks) arbitraires sans vérification de sécurité au sein du module Field UI.
*   **Risques additionnels :** Une faille RCE critique similaire a été découverte dans le module tiers *Entity List* (CVE-2026-108099), nécessitant une mise à jour spécifique. Deux failles XSS (CVE-2026-108515 et CVE-2026-108514) ont également été corrigées dans le cœur.
*   **Statut :** Aucune exploitation active n'a été signalée publiquement à ce jour, mais la criticité impose une intervention rapide.

**Recommandations :**
1.  **Mise à jour immédiate :** Passer aux versions corrigées du cœur Drupal : **11.4.10**, **11.3.19** ou **10.6.19**.
2.  **Modules tiers :** Mettre à jour le module *Entity List* vers la version **3.0.10**.
3.  **Mesure d'atténuation temporaire :** Si la mise à jour est impossible, désinstaller le module `field_ui`. Cela neutralise le vecteur d'attaque, bien que cela restreigne les capacités d'administration des champs sur le site.
4.  **Vérification :** Auditer le code personnalisé qui pourrait faire appel à la propriété `#region_callback` dans les tableaux de type `field_ui_table`, car le comportement de ces éléments a été modifié pour corriger la faille.
5.  **Pare-feu :** Utiliser des services de type WAF (comme Drupal Steward) si disponible, bien que cela ne remplace pas la nécessité d'appliquer les correctifs logiciels.

---
[Source](https://thehackernews.com/2026/10/drupal-patches-critical-core-rce-flaw.html){:target="_blank"}
