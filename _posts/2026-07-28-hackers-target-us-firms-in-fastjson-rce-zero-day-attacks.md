---
title: 'Hackers target US firms in FastJson RCE zero-day attacks'
date: 2026-07-28
permalink: /posts/2026/07/28/hackers-target-us-firms-in-fastjson-rce-zero-day-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Exploitation active de la faille RCE Zero-Day dans FastJson

Une campagne d'attaques cible actuellement des organisations américaines via une vulnérabilité critique d'exécution de code à distance (RCE) dans la bibliothèque Java open-source **FastJson**. Cette faille, exploitée activement sans interaction utilisateur ni privilèges élevés, affecte particulièrement les déploiements utilisant le format « Spring Boot fat-JAR ».

**Points clés :**
*   **Nature de la faille :** Erreur dans la logique de résolution de type permettant de charger et d'exécuter des classes malveillantes via le traitement `@type`.
*   **Portée :** Versions de FastJson 1.2.68 à 1.2.83.
*   **Cibles :** Large spectre d'industries (finance, santé, commerce, etc.), majoritairement basées aux États-Unis.
*   **Statut du correctif :** Aucun correctif n'est disponible. FastJson 1.x n'étant plus maintenu, il est peu probable qu'une mise à jour soit publiée.
*   **Facteur aggravant :** La spécification d'une classe cible lors de la désérialisation ne constitue pas une protection efficace.

**Vulnérabilité identifiée :**
*   **CVE-2026-16723 :** Vulnérabilité RCE critique.

**Recommandations :**
*   **Migration :** Passer à la version **fastjson2**, qui utilise un modèle de liste blanche et n'est pas sujette à cette vulnérabilité.
*   **Mesures conservatoires :** Si la migration est impossible, activer immédiatement le **« SafeMode »**.
*   **Évaluation de l'exposition :** Vérifier les déploiements Spring Boot. Notez que les versions antérieures à 1.2.60 et les déploiements ne fonctionnant pas sous forme de « fat-JAR » ne sont pas affectés.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-us-firms-in-fastjson-rce-zero-day-attacks/){:target="_blank"}
