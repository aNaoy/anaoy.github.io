---
title: 'Critical flaw in Protobuf library enables JavaScript code execution'
date: 2026-04-18
permalink: /posts/2026/04/18/critical-flaw-in-protobuf-library-enables-javascript-code-execution/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique d'exécution de code dans protobuf.js

La bibliothèque JavaScript `protobuf.js`, largement utilisée pour la communication de données, présente une faille critique permettant l'exécution de code à distance (RCE). Cette vulnérabilité, identifiée sous la référence **GHSA-xq3m-2v4x-88gg**, résulte d'une injection de code via des schémas malveillants non validés.

**Points clés :**
*   **Mécanisme :** La bibliothèque génère dynamiquement des fonctions via le constructeur `Function()`. Le défaut de validation des identifiants (noms des messages) dans les schémas permet à un attaquant d'injecter du code arbitraire exécuté par le serveur ou l'application.
*   **Impact :** Risque de compromission totale (accès aux variables d'environnement, identifiants, bases de données) et de mouvement latéral au sein des infrastructures.
*   **Versions affectées :** Toutes les versions jusqu'à 8.0.0 et 7.5.4 inclusivement.
*   **Statut :** Aucun cas d'exploitation active n'a été signalé, mais un code de preuve de concept (PoC) est publiquement disponible.

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions corrigées **8.0.1** ou **7.5.5**.
*   **Gestion des entrées :** Traiter tout chargement de schéma externe comme une donnée non fiable.
*   **Pratiques sécurisées :** Privilégier l'utilisation de schémas précompilés ou statiques dans les environnements de production pour limiter l'exposition.
*   **Audit :** Auditer les dépendances transitives pour identifier les usages de la bibliothèque au sein de l'architecture.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-flaw-in-protobuf-library-enables-javascript-code-execution/){:target="_blank"}
