---
title: 'Apple iPhone Air and iPhone 17 Feature A19 Chips With Spyware-Resistant Memory Safety'
date: 2025-09-10
permalink: /posts/2025/09/10/apple-iphone-air-and-iphone-17-feature-a19-chips-with-spyware-resistant-memory-safety/
tags:
- veille-cyber
- hackernews
---
**Protection Mémoire Renforcée sur les Nouveaux iPhone**

Apple introduit une nouvelle mesure de sécurité, le Memory Integrity Enforcement (MIE), sur ses derniers modèles, les iPhone 17 et iPhone Air. Cette technologie, intégrée aux puces A19 et A19 Pro, vise à assurer une protection continue de la mémoire, même lors de tâches exigeantes, afin de prévenir les attaques visant à exploiter des failles de sécurité.

**Points Clés :**

*   **Memory Integrity Enforcement (MIE)** : Une nouvelle fonctionnalité de sécurité "toujours active" pour la mémoire.
*   **Ciblage des attaques** : Destiné à contrer les acteurs malveillants, y compris les logiciels espions mercenaires, qui exploitent les failles de sécurité mémoire pour pénétrer les appareils.
*   **Base technologique** : S'appuie sur des allocateurs mémoire sécurisés, l'Enhanced Memory Tagging Extension (EMTE) en mode synchrone, et des politiques de Tag Confidentiality Enforcement (TCE).

**Vulnérabilités adressées :**

*   **Corruption de mémoire** : Le MIE est conçu pour prévenir les vulnérabilités telles que les débordements de tampon (buffer overflows) et les bugs "use-after-free". Ces types de failles permettent aux attaquants d'écraser ou d'accéder à des zones de mémoire non autorisées.
*   **Failles de l'ancienne spécification MTE** : L'EMTE, une version améliorée de l'extension de marquage mémoire d'Arm (MTE), corrige des lacunes comme l'absence de vérification de l'accès à la mémoire non marquée, facilitant ainsi les contournements par les attaquants.
*   **Attaques par exécution spéculative et canaux auxiliaires** : Le TCE vise à sécuriser l'implémentation des allocateurs mémoire contre des attaques comme TikTag, qui pouvaient fuiter des informations sur les tags mémoire en exploitant les différences d'état du cache lors de l'exécution spéculative.

**Recommandations (implicites par la nouvelle technologie) :**

*   La mise à jour vers les nouveaux modèles d'iPhone équipés de cette technologie offrira une meilleure protection contre certaines classes de vulnérabilités mémoire.
*   Le MIE transforme l'outil de débogage MTE en une fonctionnalité de sécurité significative, rendant l'exploitation des failles plus difficile.
*   Bien que d'autres fabricants comme Google et Microsoft aient introduit des fonctionnalités similaires de protection mémoire, l'approche d'Apple avec MIE est conçue pour une intégration transparente et sans impact sur les performances pour l'utilisateur.

---
[Source](https://thehackernews.com/2025/09/apple-iphone-air-and-iphone-17-feature.html){:target="_blank"}
