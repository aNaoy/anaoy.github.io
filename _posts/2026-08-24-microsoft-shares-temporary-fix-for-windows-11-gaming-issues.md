---
title: 'Microsoft shares temporary fix for Windows 11 gaming issues'
date: 2026-08-24
permalink: /posts/2026/08/24/microsoft-shares-temporary-fix-for-windows-11-gaming-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Correctif temporaire pour les problèmes de jeux sur Windows 11

Les mises à jour de Windows 11 (versions 24H2 et 25H2) déployées lors du « Patch Tuesday » d'août 2026 provoquent des instabilités critiques, notamment des crashs, des gels d'écran et des erreurs « EXCEPTION_ACCESS_VIOLATION » lors du lancement de certains jeux.

**Points clés :**
*   **Cause identifiée :** Les problèmes sont liés à des pilotes de périphériques ou composants internes équipés d'un éclairage RGB, plus précisément au fichier `inpoutx64.sys`.
*   **Impact :** Des titres comme *ARC Raiders*, *MARVEL Tōkon: Fighting Souls* et *The Finals* sont directement affectés.
*   **Vulnérabilité :** Il ne s'agit pas d'une faille de sécurité classique, mais d'une incompatibilité au niveau du pilote du noyau Windows (kernel driver) provoquée par une mise à jour système. Aucune CVE n'est associée à cet incident.

**Recommandations :**
*   **Contournement temporaire :** Microsoft recommande de désactiver le pilote `inpoutx64` via le registre Windows :
    1. Accéder à `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\inpoutx64`.
    2. Modifier la valeur « Start » par **4**.
    3. Redémarrer l'ordinateur.
*   **Précaution :** Avant toute modification, **sauvegardez votre registre**. La désactivation de ce pilote peut entraîner une perte de contrôle de l'éclairage RGB de vos périphériques.
*   **Retour arrière :** Si une perte de fonctionnalités RGB est constatée, il est possible de restaurer la valeur d'origine (généralement 3) dans le registre pour réactiver le pilote.
*   **Suivi :** Signalez tout problème via l'application « Hub de commentaires » (Feedback Hub) de Windows en attendant un correctif officiel définitif.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-shares-temporary-fix-for-windows-11-gaming-issues/){:target="_blank"}
