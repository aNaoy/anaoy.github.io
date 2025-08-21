---
title: 'CROSS-X: Generalized and Stable Cross-Cache Attack on the Linux Kernel (to appear)'
date: 2025-08-21
permalink: /posts/2025/08/21/cross-x-generalized-and-stable-cross-cache-attack-on-the-linux-kernel-to-appear/
tags:
- veille-cyber
- zerodaysfans
---
## CROSS-X : Une nouvelle attaque sur le cache du noyau Linux

Une nouvelle méthode d'attaque, nommée CROSS-X, exploite des vulnérabilités de sécurité dans la gestion du cache du noyau Linux. Cette attaque vise à contourner les mécanismes de sécurité en utilisant des manipulations subtiles du cache, permettant potentiellement à un attaquant d'obtenir des informations sensibles ou d'exécuter du code malveillant.

**Points clés :**

*   CROSS-X est une attaque généralisée et stable qui cible le cache du noyau Linux.
*   Elle exploite la façon dont les données sont stockées et récupérées dans les différents niveaux de cache de la CPU.
*   L'attaque est "généralisée" car elle ne dépend pas de faiblesses spécifiques à un type de processeur ou à une version particulière du noyau, mais cible des mécanismes fondamentaux.
*   Elle est également "stable", ce qui signifie qu'elle est plus fiable et reproductible que des attaques similaires précédentes.

**Vulnérabilités :**

Bien que l'article ne mentionne pas spécifiquement de CVE pour cette nouvelle attaque, la nature de CROSS-X suggère qu'elle pourrait tirer parti de comportements attendus mais non intentionnellement exploités des systèmes de cache, notamment la manière dont le noyau gère l'isolement entre les différents processus et le système d'exploitation lui-même au niveau du matériel de cache. Cela pourrait inclure des problèmes liés aux politiques de cohérence du cache ou à la manière dont les données sont partagées entre le noyau et l'espace utilisateur.

**Recommandations :**

Les auteurs recommandent une révision des mécanismes de gestion du cache au niveau du noyau Linux pour introduire une meilleure isolation et renforcer la sécurité contre ce type d'attaques par canal auxiliaire. Cela pourrait impliquer des modifications dans la manière dont les données sensibles sont mises en cache et invalidées. Des stratégies visant à réduire la prédictibilité des accès au cache pourraient également être envisagées.

---
[Source](https://kaist-hacking.github.io/publication/kim-crossx/){:target="_blank"}
