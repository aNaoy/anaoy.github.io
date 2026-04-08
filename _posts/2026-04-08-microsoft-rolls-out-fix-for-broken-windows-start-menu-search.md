---
title: 'Microsoft rolls out fix for broken Windows Start Menu search'
date: 2026-04-08
permalink: /posts/2026/04/08/microsoft-rolls-out-fix-for-broken-windows-start-menu-search/
tags:
- veille-cyber
- bleepingcomp
---
### Correction du dysfonctionnement de la recherche Windows 11

Microsoft a déployé un correctif côté serveur pour résoudre une panne affectant la recherche du menu Démarrer sur les appareils sous Windows 11 23H2. Ce bug, identifié sous la référence de suivi **WI1273488**, résultait d'une mise à jour de Bing destinée à optimiser les performances de recherche.

**Points clés :**
*   **Cause :** Mise à jour serveur Bing défectueuse.
*   **Symptômes :** Résultats de recherche vides ou inopérants.
*   **Vulnérabilités :** Aucune vulnérabilité de sécurité de type CVE n'est associée à cet incident ; il s'agit d'un problème de stabilité logicielle.
*   **Historique :** Le système Windows fait face à des problèmes récurrents sur le menu Démarrer, notamment des plantages liés à des paquets XAML non enregistrés lors de mises à jour cumulatives.

**Recommandations :**
*   **Application automatique :** Le correctif se déploie progressivement. Assurez-vous que l'appareil est connecté à Internet pour recevoir la mise à jour serveur.
*   **Configuration requise :** Vérifiez que la « Recherche Web » n'est pas désactivée via les stratégies de groupe (Group Policy).
*   **Cas des erreurs XAML :** Pour les plantages persistants du menu Démarrer et de l'Explorateur de fichiers liés aux paquets XAML, Microsoft recommande l'enregistrement manuel des paquets manquants via les procédures documentées sur le support technique officiel.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-rolls-out-fix-for-broken-windows-start-menu-search/){:target="_blank"}
