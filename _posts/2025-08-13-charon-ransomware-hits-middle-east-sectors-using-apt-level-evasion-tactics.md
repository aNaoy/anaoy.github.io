---
title: 'Charon Ransomware Hits Middle East Sectors Using APT-Level Evasion Tactics'
date: 2025-08-13
permalink: /posts/2025/08/13/charon-ransomware-hits-middle-east-sectors-using-apt-level-evasion-tactics/
tags:
- veille-cyber
- hackernews
---
## Charon : Ransomware Sophistiqué et Techniques d'Évasion Avancées

Une nouvelle famille de ransomware, nommée Charon, cible les secteurs public et de l'aviation au Moyen-Orient. Les acteurs de la menace démontrent des tactiques similaires à celles des groupes APT (Advanced Persistent Threat), notamment le "DLL side-loading" et l'injection de processus, leur permettant d'échapper aux logiciels de détection et de réponse (EDR).

**Points Clés :**

*   **Ciblage Spécifique :** L'utilisation d'une note de rançon personnalisée, mentionnant le nom de l'organisation victime, suggère un ciblage précis plutôt qu'une approche opportuniste.
*   **Tactiques d'Évasion :** Charon emploie le "DLL side-loading" via des fichiers légitimes (Edge.exe) pour charger une DLL malveillante (SWORDLDR), qui déploie ensuite la charge utile du ransomware. Il utilise également un driver issu du projet open-source Dark-Kill pour désactiver les solutions EDR via une attaque BYOVD (Bring Your Own Vulnerable Driver), bien que cette fonctionnalité ne soit pas encore déclenchée en production.
*   **Capacités Disruptives :** Comme d'autres ransomwares, Charon peut terminer les services et processus liés à la sécurité, ainsi que supprimer les "shadow copies" et les sauvegardes pour entraver la récupération.
*   **Optimisation de l'Encryption :** Le ransomware utilise le multithreading et des techniques de chiffrement partiel pour accélérer le processus de chiffrement des fichiers.
*   **Convergence avec Earth Baxia :** Les similitudes techniques avec les opérations du groupe Earth Baxia (lié à la Chine) soulèvent la possibilité d'une implication directe, d'une opération de faux drapeau, ou du développement indépendant de tactiques similaires par un nouvel acteur.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques exploitées dans cette campagne. Cependant, il détaille l'utilisation du "DLL side-loading", une technique courante qui exploite la manière dont les applications chargent les bibliothèques de liens dynamiques. L'attaque BYOVD mentionnée exploite la confiance accordée aux drivers, même s'ils proviennent de sources externes.

**Recommandations :**

L'article souligne l'importance de surveiller les activités de processus suspectes, l'utilisation de LOLBins (Living Off The Land Binaries) et d'autres Tactiques, Techniques et Procédures (TTPs). La convergence croissante des tactiques APT avec les opérations de ransomware accroît le risque, combinant des méthodes d'évasion sophistiquées avec un impact commercial immédiat dû au chiffrement des données.

---
[Source](https://thehackernews.com/2025/08/charon-ransomware-hits-middle-east.html){:target="_blank"}
