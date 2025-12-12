---
title: 'Abusing DLLs EntryPoint for the Fun, (Fri, Dec 12th)'
date: 2025-12-12
permalink: /posts/2025/12/12/abusing-dlls-entrypoint-for-the-fun-fri-dec-12th/
tags:
- veille-cyber
- sans-isc
---
**Exploitation de l'Entry Point des DLLs**

Les bibliothèques de liens dynamiques (DLL) sous Windows sont des fichiers PE similaires aux exécutables, mais elles exportent des fonctions appelables par d'autres programmes. Une caractéristique importante des fichiers PE, y compris les DLL, est leur "EntryPoint". Pour une DLL, cet EntryPoint pointe vers une fonction nommée `DllMain`. Le code à cette adresse s'exécute lorsque la DLL est chargée ou déchargée, recevant des informations sur la raison de cet appel (attachement au processus, attachement à un thread, détachement du processus, détachement d'un thread). Bien qu'optionnelle, la fonction `DllMain` est souvent utilisée pour initialiser la DLL. Microsoft déconseille d'y effectuer des actions sensibles.

Les logiciels malveillants peuvent être déployés sous forme de DLL pour échapper à la détection. Des outils comme `regsvr32.exe` et `rundll32.exe` sont couramment utilisés pour interagir avec les DLL. `regsvr32.exe` permet d'enregistrer des DLL, tandis que `rundll32.exe` peut appeler des fonctions spécifiques exportées par une DLL.

Lors de l'analyse de DLL suspectes, les experts se concentrent souvent sur les fonctions exportées, ignorant potentiellement le code malveillant dissimulé dans la fonction `DllMain` de l'EntryPoint. Il est possible de créer une DLL qui exécute automatiquement du code dès son chargement, indépendamment de l'appel à une fonction exportée. Par exemple, une DLL malveillante pourrait lancer un processus tel que `calc.exe` lors de son chargement via `LoadLibraryA()`.

**Points Clés :**

*   Les DLL possèdent un "EntryPoint" (`DllMain`) qui s'exécute lors de leur chargement ou déchargement.
*   Les acteurs malveillants peuvent dissimuler du code dans `DllMain` pour une exécution furtive.
*   Les outils comme `regsvr32.exe` et `rundll32.exe` sont des vecteurs d'attaque courants utilisant des DLL.

**Vulnérabilités / Exploitation :**

*   L'exploitation réside dans le fait que l'analyse de sécurité se concentre souvent sur les fonctions exportées et néglige le code exécuté à l'EntryPoint (`DllMain`) lors du chargement de la DLL.

**Recommandations :**

*   Toujours examiner le contenu de la fonction `DllMain` lors de l'analyse de DLL suspectes.
*   Éviter d'effectuer des opérations sensibles dans la fonction `DllMain` lors du développement de DLL légitimes.

---
[Source](https://isc.sans.edu/diary/rss/32562){:target="_blank"}
