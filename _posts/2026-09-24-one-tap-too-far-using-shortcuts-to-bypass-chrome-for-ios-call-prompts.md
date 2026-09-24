---
title: 'One Tap Too Far: Using Shortcuts to Bypass Chrome for iOS Call Prompts'
date: 2026-09-24
permalink: /posts/2026/09/24/one-tap-too-far-using-shortcuts-to-bypass-chrome-for-ios-call-prompts/
tags:
- veille-cyber
- zerodaysfans
---
### Contournement des alertes de sécurité dans Chrome pour iOS via l'application Raccourcis

Une vulnérabilité dans Chrome pour iOS permettait de contourner les protections du navigateur lors de l'ouverture d'applications tierces via des schémas d'URL personnalisés. En exploitant l'application native « Raccourcis » (Shortcuts) d'Apple, un site web pouvait déclencher des actions sensibles, comme initier un appel téléphonique ou un FaceTime, sans l'approbation explicite de l'utilisateur.

#### Points clés
* **Mécanisme de confiance abusif :** Chrome considérait `shortcuts://` et `workflow://` comme des applications Apple de confiance, omettant l'alerte de confirmation habituelle lors de l'ouverture de liens externes.
* **Chaînage de requêtes :** L'application Raccourcis supporte le standard `x-callback-url`, permettant de spécifier une URL cible à exécuter après le succès, l'échec ou l'annulation d'un raccourci.
* **Bypass de sécurité :** Un attaquant pouvait insérer une URL malveillante (ex: `tel://`) dans les paramètres de rappel (`x-error`, `x-success`). Chrome vérifiait uniquement le lancement du raccourci, mais ne contrôlait pas l'URL finale exécutée par iOS une fois le raccourci terminé, contournant ainsi les vérifications de sécurité du navigateur.

#### Vulnérabilité
* **CVE-2026-13795 :** Ce contournement de permissions permettait d'exécuter des actions non autorisées (appels, FaceTime) après un seul clic, en utilisant l'application Raccourcis comme intermédiaire pour échapper à la politique de lancement d'applications de Chrome.

#### Recommandation
* **Mise à jour :** Appliquer les dernières mises à jour de Chrome sur iOS. Le correctif implémenté par Chromium impose désormais une alerte de confirmation utilisateur avant toute ouverture d'une URL `shortcuts://` ou `workflow://`, empêchant ainsi le lancement silencieux de toute chaîne de rappels malveillants.

---
[Source](https://blog.doyensec.com/2026/09/24/chrome-ios-policy-bypass.html){:target="_blank"}
