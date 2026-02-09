---
title: 'Password guessing without AI: How attackers build targeted wordlists'
date: 2026-02-09
permalink: /posts/2026/02/09/password-guessing-without-ai-how-attackers-build-targeted-wordlists/
tags:
- veille-cyber
- bleepingcomp
---
**L'Art de Constituer des Listes de Mots Ciblant les Mots de Passe**

Les stratégies d'attaques contre les mots de passe s'appuient souvent sur une méthode simple mais efficace : la collecte de termes pertinents liés à une organisation pour créer des listes de mots de passe ciblées. Plutôt que d'utiliser des techniques d'intelligence artificielle complexes, les attaquants exploitent le langage utilisé par les entreprises et leurs employés. Des outils comme CeWL (Custom Word List generator) permettent de parcourir le contenu public d'une organisation (sites web, documentations) afin d'en extraire un vocabulaire spécifique. Ce vocabulaire est ensuite utilisé comme base pour générer des variations de mots de passe plausibles, souvent par l'ajout de chiffres, de symboles ou de modifications de casse. Ces listes de mots personnalisées sont ensuite employées avec des outils comme Hashcat pour tenter de déchiffrer des mots de passe compromis, ou pour attaquer des services d'authentification en direct de manière discrète.

**Points Clés :**

*   Les mots de passe sont souvent basés sur le langage spécifique à une organisation, créant un point faible pour la sécurité.
*   Les attaquants n'utilisent pas forcément l'IA, mais préfèrent construire des listes de mots ciblées à partir du contenu public des entreprises.
*   Des outils comme CeWL facilitent la création de ces listes en crawlant les sites web.
*   Ces listes, combinées à des mutations de mots de passe courantes, permettent de générer des candidats crédibles.
*   La complexité des mots de passe, si elle est basée sur des termes contextuels, ne garantit pas une sécurité suffisante.

**Vulnérabilités et Risques :**

*   Utilisation de mots de passe basés sur le nom de l'entreprise, ses produits, des termes internes ou du jargon industriel.
*   Mots de passe contenant des noms de services, des noms d'utilisateur ou des variations de ceux-ci.
*   Mots de passe qui, malgré leur longueur ou leur complexité apparente, sont facilement devinables en raison de leur origine contextuelle (ex: `NomEntreprise123!`).
*   Exploitation de mots de passe déjà compromis dans des violations de données antérieures.

**Recommandations :**

*   **Bloquer les mots de passe dérivés du contexte :** Interdire l'utilisation de termes liés à l'entreprise, aux produits, aux projets internes ou au secteur d'activité.
*   **Bloquer les mots de passe compromis connus :** Utiliser des bases de données de mots de passe ayant fuité pour empêcher leur réutilisation.
*   **Imposer une longueur minimale importante :** Privilégier des phrases de passe d'au moins 15 caractères pour une meilleure résistance aux attaques par force brute.
*   **Activer l'authentification multi-facteurs (MFA) :** C'est une couche de sécurité essentielle qui limite l'impact de la compromission d'un mot de passe.

---
[Source](https://www.bleepingcomputer.com/news/security/password-guessing-without-ai-how-attackers-build-targeted-wordlists/){:target="_blank"}
