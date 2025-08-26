---
title: 'New AI attack hides data-theft prompts in downscaled images'
date: 2025-08-26
permalink: /posts/2025/08/26/new-ai-attack-hides-data-theft-prompts-in-downscaled-images/
tags:
- veille-cyber
- bleepingcomp
---
**Espionnage Visuel : L'Art de Cacher des Ordres Malveillants dans les Images D'IA**

Des chercheurs ont découvert une méthode d'attaque novatrice qui exploite la manière dont les systèmes d'intelligence artificielle traitent les images pour voler des données. Cette technique consiste à dissimuler des instructions malveillantes au sein d'images, rendant celles-ci invisibles à l'œil humain, mais lisibles par l'IA une fois que la qualité de l'image est dégradée lors d'un processus de réduction de taille.

**Fonctionnement de l'attaque :**

Lorsque des utilisateurs soumettent des images à des systèmes d'IA, ces derniers les réduisent souvent en résolution pour optimiser les performances et les coûts. Les algorithmes de rééchantillonnage utilisés pour cette réduction (comme l'interpolation voisine la plus proche, bilinéaire ou bicubique) peuvent introduire des artefacts. Si une image est spécialement conçue, ces artefacts peuvent révéler des motifs cachés, tels que du texte noir sur fond rouge après une réduction bicubique. L'IA interprète ce texte comme une partie des instructions de l'utilisateur, exécutant ainsi des commandes non autorisées, ce qui peut mener à des fuites de données.

Dans un exemple concret, cette méthode a permis d'exfiltrer des données du calendrier Google vers une adresse e-mail arbitraire via Gemini CLI, en utilisant Zapier MCP avec une option de confiance permettant d'approuver les appels d'outils sans confirmation de l'utilisateur.

**Systèmes Affectés :**

L'attaque peut être ajustée pour différents modèles d'IA en fonction de leur algorithme de réduction de taille. Les systèmes testés avec succès incluent :

*   Google Gemini CLI
*   Vertex AI Studio (avec backend Gemini)
*   L'interface web de Gemini
*   L'API Gemini via le CLI llm
*   Google Assistant sur Android
*   Genspark

Il est probable que cette vulnérabilité s'étende à d'autres outils d'IA. Un outil open-source nommé Anamorpher a été développé pour créer des images exploitant cette technique pour diverses méthodes de réduction.

**Points Clés :**

*   Injection de prompts malveillants dans les images traitées par l'IA.
*   Exploitation des artefacts créés par la réduction de la qualité des images.
*   Possibilité de fuite de données et d'actions non autorisées par l'IA.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques associés à cette attaque, mais il met en évidence une vulnérabilité intrinsèque à la manière dont certains systèmes d'IA traitent les images lors de la réduction de leur résolution.

**Recommandations :**

*   **Restriction de Dimensions :** Les systèmes d'IA devraient imposer des limites de dimensions lors du téléchargement d'images par les utilisateurs.
*   **Aperçu de l'Image Traitée :** En cas de réduction nécessaire, proposer un aperçu du résultat envoyé au modèle linguistique.
*   **Confirmation pour Actions Sensibles :** Solliciter la confirmation explicite des utilisateurs pour les appels d'outils sensibles, surtout si du texte est détecté dans une image.
*   **Conception Sécurisée :** Mettre en œuvre des modèles de conception sécurisés et des défenses systématiques pour atténuer les injections de prompts, y compris les injections multimodales.

---
[Source](https://www.bleepingcomputer.com/news/security/new-ai-attack-hides-data-theft-prompts-in-downscaled-images/){:target="_blank"}
