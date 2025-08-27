---
title: 'Interesting Technique to Launch a Shellcode, (Wed, Aug 27th)'
date: 2025-08-27
permalink: /posts/2025/08/27/interesting-technique-to-launch-a-shellcode-wed-aug-27th/
tags:
- veille-cyber
- sans-isc
---
### Exécution furtive de code via l'API Windows

Une technique d'exécution de code malveillant contournant les solutions de sécurité (EDR) est décrite. Plutôt que les méthodes classiques impliquant l'allocation de mémoire exécutable (`VirtualAlloc`) et la création de nouveaux threads (`CreateThread`), cette approche exploite l'API Windows `CallWindowProcA`.

Cette fonction, normalement utilisée pour la gestion des interfaces graphiques, peut être détournée pour exécuter un pointeur de fonction sans nécessiter de nouveau thread, rendant ainsi l'activité plus discrète aux yeux des systèmes de détection. Le processus implique :

*   L'utilisation d'un script PowerShell lancé par un exécutable Windows.
*   La lecture de fichiers de configuration (ici `.Paa` et `.Mde`) contenant des portions de code.
*   L'allocation de mémoire via des appels similaires à `VirtualAlloc`.
*   La copie du shellcode dans ces régions mémoire allouées en utilisant `Marshal.Copy`.
*   L'obtention d'un délégué pour la fonction `CallWindowProcA` de la bibliothèque `User32.dll`.
*   L'invocation de ce délégué avec les pointeurs des régions mémoire contenant le shellcode, déclenchant ainsi son exécution dans le contexte du processus courant.

**Points clés :**

*   **Contournement EDR :** La technique évite les signaux d'alerte associés à `CreateThread`.
*   **Apparence légitime :** L'utilisation de `CallWindowProcA` est une pratique courante dans les applications graphiques, aidant à masquer l'activité malveillante.
*   **Exécution dans le processus courant :** Le code malveillant s'exécute dans le contexte du processus légitime, compliquant l'analyse.

**Vulnérabilités exploitées :**

Bien qu'aucun CVE spécifique ne soit mentionné dans l'article, la vulnérabilité réside dans la capacité de l'API `CallWindowProcA` à exécuter n'importe quel pointeur de fonction fourni, sans validation préalable de son origine ou de sa nature. L'article ne détaille pas de vulnérabilité logicielle spécifique, mais plutôt une utilisation abusive d'une fonctionnalité système.

**Recommandations :**

*   **Surveillance des appels API inhabituels :** Porter une attention particulière à l'utilisation de `CallWindowProcA` en dehors des contextes GUI typiques, ou lorsqu'elle est appelée avec des pointeurs de fonction issus de mémoire non conventionnellement allouée ou modifiée.
*   **Analyse comportementale :** Les solutions de sécurité devraient renforcer leur analyse comportementale pour détecter les schémas d'exécution de code qui divergent des opérations normales.
*   **Analyse de flux de données :** Identifier les scripts PowerShell qui lisent des fichiers à des emplacements inhabituels, et qui utilisent des fonctions d'invocation comme `IEX`.
*   **Détection de l'allocation mémoire :** Maintenir la capacité à détecter les allocations mémoire suspectes et leur utilisation ultérieure pour l'exécution de code.

---
[Source](https://isc.sans.edu/diary/rss/32238){:target="_blank"}
