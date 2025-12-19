---
title: 'DLLs &#x26; TLS Callbacks, (Fri, Dec 19th)'
date: 2025-12-19
permalink: /posts/2025/12/19/dlls-x26-tls-callbacks-fri-dec-19th/
tags:
- veille-cyber
- sans-isc
---
**Utilisation des rappels TLS dans les DLL : une nouvelle voie d'exécution**

Les rappels TLS (Thread Local Storage) représentent un mécanisme d'exécution sous Windows permettant d'exécuter du code automatiquement au démarrage d'un processus ou d'un thread, avant même que le point d'entrée normal du programme ne soit atteint. Bien que cette fonctionnalité ait été étudiée dans le contexte des exécutables, son application aux bibliothèques à liens dynamiques (DLL) offre de nouvelles perspectives, notamment pour des actions malveillantes ou des analyses de sécurité.

Le format PE (Portable Executable) de Windows inclut un répertoire TLS qui décrit l'emplacement et la taille des données TLS, ainsi qu'une liste de fonctions de rappel. Ces fonctions peuvent être intégrées dans une DLL via des directives de compilation spécifiques.

Lorsqu'une DLL contenant un rappel TLS est chargée, cette fonction de rappel s'exécute avant la fonction `DllMain` standard. Cela présente un intérêt particulier pour les analystes de sécurité.

**Points clés :**

*   Les rappels TLS permettent l'exécution de code avant le point d'entrée principal d'un programme ou d'une DLL.
*   Ce mécanisme peut être utilisé pour exécuter du code arbitraire dès le chargement d'une DLL, avant même `DllMain`.
*   Les outils d'analyse statique devraient prendre en compte la détection des rappels TLS dans les fichiers PE.
*   La configuration des débogueurs est cruciale pour la détection. Un débogueur configuré pour ignorer les rappels TLS ne les exécutera pas et ne s'arrêtera pas à ces points.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article. Cependant, l'exploitation des rappels TLS pourrait potentiellement être utilisée dans le cadre de :

*   **Chargement de code malveillant :** Permettre à un logiciel malveillant de s'exécuter discrètement dès le chargement d'une DLL compromise.
*   **Évasion de la détection :** Contourner certaines mesures de sécurité qui surveillent principalement le point d'entrée principal ou `DllMain`.

**Recommandations :**

*   **Analyse statique :** Les outils d'analyse statique doivent être mis à jour pour identifier la présence et le contenu des rappels TLS dans les fichiers DLL.
*   **Analyse dynamique :** Lors de l'utilisation de débogueurs pour l'analyse dynamique, il est impératif de vérifier leur configuration pour s'assurer qu'ils sont réglés pour intercepter et potentiellement arrêter l'exécution des rappels TLS. Une configuration adéquate permettra de découvrir ces fonctions de rappel et leur comportement.

---
[Source](https://isc.sans.edu/diary/rss/32580){:target="_blank"}
