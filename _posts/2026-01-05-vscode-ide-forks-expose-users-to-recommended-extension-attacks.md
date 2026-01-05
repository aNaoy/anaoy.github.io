---
title: 'VSCode IDE forks expose users to "recommended extension" attacks'
date: 2026-01-05
permalink: /posts/2026/01/05/vscode-ide-forks-expose-users-to-recommended-extension-attacks/
tags:
- veille-cyber
- bleepingcomp
---
## Attaques d'extensions recommandées sur les forks de VSCode

Certains environnements de développement intégrés (IDE) basés sur l'IA, tels que Cursor, Windsurf et Google Antigravity, dérivés de Microsoft VSCode, présentent un risque pour la sécurité. Ces plateformes, qui ne peuvent pas utiliser directement le magasin d'extensions officiel de Microsoft en raison de restrictions de licence, s'appuient sur OpenVSX, une alternative open-source.

Cependant, ces IDE héritent de listes d'extensions recommandées préconfigurées qui pointent vers le marché Microsoft. Le problème réside dans le fait que certaines de ces extensions recommandées n'existent pas dans le registre OpenVSX. Cela laisse des "espaces de noms" de publication ouverts et non réclamés. Des acteurs malveillants pourraient exploiter cette situation en enregistrant ces espaces de noms et en y publiant des extensions malveillantes, profitant ainsi de la confiance des utilisateurs dans les recommandations de l'IDE pour distribuer des logiciels nuisibles.

Les chercheurs de Koi ont signalé ce problème à Google, Windsurf et Cursor. Google a réagi en supprimant des recommandations d'extensions, tandis que Cursor et Windsurf n'ont pas encore répondu. Pour pallier ce risque immédiat, les chercheurs de Koi ont revendiqué les espaces de noms vulnérables et y ont publié des extensions fictives pour empêcher leur exploitation. Des mesures sont également prises avec l'opérateur d'OpenVSX pour renforcer la sécurité du registre. Aucune exploitation de cette vulnérabilité n'a été confirmée avant la découverte.

**Points Clés :**

*   Des IDE dérivés de VSCode recommandent des extensions qui n'existent pas sur OpenVSX, une marketplace alternative.
*   Les espaces de noms non réclamés peuvent être enregistrés par des attaquants pour distribuer des logiciels malveillants.
*   Google a corrigé le problème, tandis que Cursor et Windsurf sont toujours en attente de réponse.
*   Des chercheurs ont préempté l'exploitation en revendiquant des espaces de noms et en y publiant des extensions inertes.

**Vulnérabilités :**

*   Les extensions recommandées par certains IDE dérivés de VSCode (Cursor, Windsurf, Google Antigravity) n'existent pas dans le registre OpenVSX, laissant des espaces de noms de publication ouverts.
*   Aucun CVE spécifique n'est mentionné dans l'article pour cette vulnérabilité, car il s'agit d'un défaut de configuration et de disponibilité d'extensions plutôt que d'une faille logicielle intrinsèque dans VSCode ou OpenVSX eux-mêmes.

**Recommandations :**

*   Les utilisateurs d'IDE dérivés de VSCode doivent vérifier manuellement les recommandations d'extensions.
*   Il est conseillé de consulter directement le registre OpenVSX pour confirmer que les extensions proviennent d'éditeurs réputés.

---
[Source](https://www.bleepingcomputer.com/news/security/vscode-ide-forks-expose-users-to-recommended-extension-attacks/){:target="_blank"}
