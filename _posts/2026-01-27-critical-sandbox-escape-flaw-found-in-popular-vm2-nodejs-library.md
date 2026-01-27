---
title: 'Critical sandbox escape flaw found in popular vm2 NodeJS library'
date: 2026-01-27
permalink: /posts/2026/01/27/critical-sandbox-escape-flaw-found-in-popular-vm2-nodejs-library/
tags:
- veille-cyber
- bleepingcomp
---
### Évasion Critique de la Sandbox dans la Bibliothèque Node.js vm2

Une vulnérabilité critique dans la bibliothèque Node.js vm2, référencée **CVE-2026-22709**, permet à des attaquants de s'échapper de l'environnement sandbox isolé et d'exécuter du code arbitraire sur le système hôte.

La bibliothèque vm2, conçue pour exécuter du code JavaScript non fiable dans un contexte sécurisé sans accès au système de fichiers, a été largement utilisée dans diverses plateformes. Cependant, elle a été officiellement délaissée en 2023 en raison de vulnérabilités répétées d'évasion de sandbox, la rendant dangereuse pour le code non fiable. Malgré cela, le projet a été relancé avec la version 3.10.0 qui visait à corriger les vulnérabilités connues.

La faille actuelle découle d'un problème de "sanitisation insuffisante" des "Promises" par vm2. Bien que les callbacks internes de vm2 soient nettoyés, les fonctions asynchrones retournent une Promise globale dont les callbacks `.then()` et `.catch()` ne sont pas correctement traités. Cela permet aux attaquants de contourner les protections et d'exécuter du code malveillant.

Des correctifs ont été déployés dans les versions 3.10.1 et 3.10.2 pour adresser cette vulnérabilité. Le mainteneur a confirmé que toutes les vulnérabilités divulguées ont été corrigées dans la version 3.10.3.

**Points Clés :**

*   **Bibliothèque affectée :** vm2 (une bibliothèque Node.js pour créer des environnements sandbox)
*   **Nature de la vulnérabilité :** Évasion de sandbox permettant l'exécution de code arbitraire sur le système hôte.
*   **Cause :** Mauvaise gestion (sanitisation insuffisante) des callbacks des Promises globales retournées par les fonctions asynchrones.
*   **Statut du projet :** Officiellement délaissé en 2023, mais relancé par la suite avec des mises à jour.
*   **Popularité :** Très répandue sur npm avec environ un million de téléchargements hebdomadaires.

**Vulnérabilités :**

*   **CVE-2026-22709 :** Vulnérabilité critique d'évasion de sandbox due à une mauvaise sanitisation des callbacks de Promise.
*   **Vulnérabilités antérieures :**
    *   CVE-2022-36067
    *   CVE-2023-29017
    *   CVE-2023-30547

**Recommandations :**

*   **Mettre à jour immédiatement :** Il est fortement recommandé de mettre à jour vers la dernière version disponible de vm2 (actuellement 3.10.3), qui corrige toutes les vulnérabilités connues.
*   **Éviter d'exécuter du code non fiable :** Compte tenu de l'historique des vulnérabilités, l'utilisation de vm2 pour exécuter du code non fiable est déconseillée, même après les correctifs, à moins que des mesures de sécurité supplémentaires ne soient mises en place.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-sandbox-escape-flaw-discovered-in-popular-vm2-nodejs-library/){:target="_blank"}
