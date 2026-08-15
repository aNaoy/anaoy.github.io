---
title: 'How Anthropic plans to watermark Claudes AI-generated text'
date: 2026-08-15
permalink: /posts/2026/08/15/how-anthropic-plans-to-watermark-claudes-ai-generated-text/
tags:
- veille-cyber
- bleepingcomp
---
### Implémentation du tatouage numérique (watermarking) pour les textes générés par Claude

Anthropic déploie une solution de tatouage numérique invisible pour ses modèles Claude afin de se conformer à l'EU AI Act. Contrairement aux méthodes ajoutant des caractères cachés, cette approche modifie la distribution statistique des mots générés sans altérer la qualité, la créativité ou la vitesse de réponse du modèle.

**Points clés :**
*   **Technologie :** Basée sur *SynthID-Text* de Google DeepMind, cette technique influence la sélection des jetons (tokens) lors de la génération en utilisant une clé secrète, créant une signature statistique indétectable par l'utilisateur mais identifiable par un outil dédié.
*   **Neutralité :** Le processus n'impacte pas le contenu et ne nécessite aucun jeton supplémentaire.
*   **Exceptions :** Le tatouage est omis lorsque le modèle doit fournir une réponse factuelle unique (ex: calculs) ou du code informatique fonctionnel, où toute altération risquerait de rendre le résultat erroné.
*   **Limites :** Le système mesure une probabilité de génération par Claude. Il est moins efficace sur des textes courts, des contenus fortement réécrits par des humains ou si le modèle manque d'entropie (choix limités). Il ne permet pas d'identifier si un autre modèle d'IA a été utilisé.
*   **Accessibilité :** Anthropic prévoit de mettre à disposition une API pour la détection du tatouage. Pour les fichiers images (PNG, JPG, SVG), l'entreprise privilégie l'utilisation de métadonnées C2PA signées cryptographiquement.

**Recommandations :**
*   **Pour les utilisateurs :** Ne pas considérer le tatouage comme une preuve absolue d'origine, car une réécriture humaine complète suffit à effacer la signature statistique.
*   **Pour les développeurs/vérificateurs :** Utiliser l'API officielle d'Anthropic pour obtenir une estimation fiable, tout en gardant à l'esprit que la fiabilité de la détection augmente avec la longueur du texte analysé.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/how-anthropic-plans-to-watermark-claudes-ai-generated-text/){:target="_blank"}
