---
title: 'Achieving the impossible: XSS in innerHTML without equals'
date: 2026-11-18
permalink: /posts/2026/11/18/achieving-the-impossible-xss-in-innerhtml-without-equals/
tags:
- veille-cyber
- zerodaysfans
---
### Contourner l'impossible : XSS via `<selectedcontent>` sans signe égal

Une nouvelle technique permet d'exécuter du code JavaScript dans un contexte `innerHTML` sans utiliser de signe égal (`=`), défiant ainsi ce qui était considéré comme une impossibilité technique dans le domaine du Cross-Site Scripting (XSS).

**Points clés :**
* **L'élément clé :** La découverte repose sur l'utilisation de la balise `<selectedcontent>`, un élément récent introduit dans Chrome et Safari.
* **Mécanisme de clonage :** Lorsqu'il est utilisé à l'intérieur d'un élément `<select>`, `<selectedcontent>` clone automatiquement les nœuds enfants de l'option sélectionnée.
* **Détournement du flux :** La recherche a démontré que le clonage d'un élément `<script>` encapsulé dans un namespace SVG (`<svg><script>`) permet de contourner le mécanisme de sécurité qui empêche l'exécution des scripts injectés via `innerHTML`.
* **État actuel :** Bien que Chromium ait corrigé ce comportement (en marquant le script comme « déjà démarré » lors du clonage), la vulnérabilité reste exploitable dans Safari (version 27.2).

**Vulnérabilités :**
* L'implémentation initiale des navigateurs omettait de définir correctement l'indicateur `already started` pour les éléments `<script>` SVG lors du clonage DOM, permettant une exécution non autorisée de code. Il n'existe pas de CVE spécifique mentionnée pour cette technique expérimentale, celle-ci étant davantage une découverte de recherche sur les comportements des moteurs de rendu.

**Recommandations :**
* **Mises à jour des navigateurs :** S'assurer que les navigateurs sont tenus à jour vers les versions les plus récentes, car le correctif a déjà été implémenté dans le projet Chromium.
* **Sanitisation rigoureuse :** Ne pas se reposer uniquement sur les limitations syntaxiques (comme l'interdiction du signe `=`) pour sécuriser les entrées utilisateur. Utiliser des bibliothèques de confiance comme DOMPurify pour nettoyer les entrées avant toute insertion dans le DOM.
* **Politique de sécurité (CSP) :** Implémenter une politique de sécurité du contenu (CSP) stricte qui restreint l'exécution de scripts en ligne, ce qui neutraliserait ce vecteur d'attaque même en cas de contournement de la logique DOM.

---
[Source](https://portswigger.net/research/achieving-the-impossible-xss-in-innerhtml-without-equals){:target="_blank"}
