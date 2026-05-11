---
title: 'LLMs and Text-in-Text Steganography'
date: 2026-05-11
permalink: /posts/2026/05/11/llms-and-text-in-text-steganography/
tags:
- veille-cyber
- schneier
---
### Stéganographie et LLMs : Les limites de l'obfuscation textuelle

L'utilisation des modèles de langage (LLM) pour la stéganographie — l'art de dissimuler des messages dans un texte apparemment anodin — soulève des défis de sécurité croissants. Les échanges mettent en lumière que les techniques traditionnelles d'obfuscation, comme la modification phonologique ou lexicale, sont de moins en moins efficaces face aux capacités d'interprétation des LLMs modernes.

**Points clés :**
*   **Résilience des modèles :** Des modèles de langage, même de petite taille (environ 4 milliards de paramètres), parviennent à décoder facilement des textes volontairement altérés ou phonétiquement modifiés.
*   **Niveaux de stéganographie :** L'efficacité de la dissimulation dépend de la "couche" linguistique visée. Plus le message est intégré à un niveau sémantique élevé, plus il est cohérent, mais plus il risque de dégrader la lisibilité du texte porteur.
*   **Techniques obsolètes :** Les méthodes simples de masquage visuel (texte blanc sur fond blanc ou noir sur noir) restent inefficaces contre l'analyse automatisée, ces approches relevant davantage de la censure que d'une véritable stéganographie.

**Vulnérabilités :**
*   Il n'existe pas de CVE spécifique associée, car il s'agit d'une limite inhérente à la puissance de traitement sémantique des IA plutôt que d'une faille de code logicielle. Le risque réside dans la capacité des LLMs à "nettoyer" le bruit et à extraire des intentions cachées, facilitant ainsi la détection de messages secrets dans des flux de données chiffrées ou obfusquées.

**Recommandations :**
*   **Ne pas se fier à l'obfuscation textuelle :** Les méthodes basées sur la simple modification de texte ne constituent pas une protection réelle contre l'analyse par des systèmes d'IA.
*   **Approche multicouche :** Pour la confidentialité, privilégiez le chiffrement robuste (AES-256) plutôt que des techniques stéganographiques textuelles, dont la sécurité est devenue obsolète face aux capacités de traitement en langage naturel.
*   **Veille technologique :** La capacité des modèles à déchiffrer des schémas sémantiques complexes rend nécessaire une remise en question constante des méthodes de communication clandestine dans les environnements numériques.

---
[Source](https://www.schneier.com/blog/archives/2026/05/llms-and-text-in-text-steganography.html){:target="_blank"}
