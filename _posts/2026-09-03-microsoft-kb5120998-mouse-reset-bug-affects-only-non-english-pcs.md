---
title: 'Microsoft: KB5120998 mouse reset bug affects only non-English PCs'
date: 2026-09-03
permalink: /posts/2026/09/03/microsoft-kb5120998-mouse-reset-bug-affects-only-non-english-pcs/
tags:
- veille-cyber
- bleepingcomp
---
### Bug de réinitialisation des paramètres de souris sous Windows 11

La mise à jour facultative KB5120998 (août 2026) pour Windows 11 (versions 25H2 et 24H2) entraîne une réinitialisation automatique des préférences de personnalisation de la souris (curseurs et animations) vers leurs paramètres par défaut.

**Points clés :**
*   **Périmètre :** Le problème est strictement limité aux systèmes Windows configurés dans des langues autres que l'anglais.
*   **Cause technique :** Une défaillance dans les composants de code gérant le chargement des paramètres dans les versions localisées de Windows empêche la restauration des préférences personnalisées.
*   **Installation :** Étant une mise à jour de prévisualisation, elle n'est installée que si l'utilisateur la sollicite manuellement ou si l'option « Obtenir les dernières mises à jour dès qu'elles sont disponibles » est activée.
*   **Effets collatéraux :** La mise à jour KB5120998 provoque également, sur certains appareils, la réinitialisation non désirée des paramètres du bureau.

**Vulnérabilités :**
*   Aucune CVE associée (il s'agit d'un bug fonctionnel et non d'une faille de sécurité).

**Recommandations :**
*   **Utilisateurs affectés :** En l'absence de correctif immédiat, il est conseillé aux utilisateurs de systèmes non anglophones de désinstaller la mise à jour KB5120998 s'ils rencontrent des problèmes de configuration.
*   **Prévention :** Désactiver l'option « Obtenir les dernières mises à jour dès qu'elles sont disponibles » dans les paramètres de Windows Update pour éviter l'installation automatique de mises à jour de prévisualisation (preview) non critiques.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-kb5120998-mouse-reset-bug-affects-only-non-english-pcs/){:target="_blank"}
