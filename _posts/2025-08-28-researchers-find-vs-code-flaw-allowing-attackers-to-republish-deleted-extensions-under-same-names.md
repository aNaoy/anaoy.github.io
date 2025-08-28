---
title: 'Researchers Find VS Code Flaw Allowing Attackers to Republish Deleted Extensions Under Same Names'
date: 2025-08-28
permalink: /posts/2025/08/28/researchers-find-vs-code-flaw-allowing-attackers-to-republish-deleted-extensions-under-same-names/
tags:
- veille-cyber
- hackernews
---
### Brèche dans le Marketplace VS Code : Réutilisation des noms d'extensions supprimées

Une faille dans le marketplace de Visual Studio Code permet aux attaquants de réutiliser les noms d'extensions précédemment supprimées. Cette découverte a été faite par ReversingLabs lors de l'analyse d'une extension malveillante ("ahbanC.shiba") partageant un nom similaire à des extensions précédemment signalées ("ahban.shiba"). Ces extensions sont conçues pour télécharger une charge utile PowerShell qui chiffre des fichiers et exige une rançon en Shiba Inu token.

La documentation de VS Code stipule que le nom d'une extension doit être unique sur le Marketplace. Cependant, la recherche a révélé qu'une fois une extension supprimée, son nom peut être réutilisé. Contrairement au Python Package Index (PyPI), VS Code ne semble pas avoir de mécanisme pour empêcher la réutilisation des noms d'extensions malveillantes supprimées.

Ce comportement, similaire à celui observé sur PyPI où les noms de packages supprimés peuvent être repris, ouvre la porte à des attaques de type "supply chain" où des acteurs malveillants pourraient republier des extensions populaires supprimées sous leur nom d'origine pour distribuer des logiciels malveillants. Cela s'inscrit dans une tendance plus large où les acteurs malveillants cherchent à exploiter les dépôts open-source.

L'article mentionne également la découverte de huit packages npm malveillants utilisant des techniques d'obfuscation avancées pour voler des informations sensibles de navigateurs Chrome, notamment des mots de passe, des données de cartes de crédit et des informations de portefeuilles de cryptomonnaies.

**Points Clés :**

*   Une vulnérabilité dans le marketplace de Visual Studio Code permet la réutilisation des noms d'extensions supprimées.
*   Les attaquants peuvent exploiter cette faille pour distribuer des extensions malveillantes sous des noms familiers et apparemment légitimes.
*   Cette situation représente un risque accru pour la sécurité de la chaîne d'approvisionnement logicielle.

**Vulnérabilités :**

*   Pas de CVE spécifié dans l'article. La vulnérabilité réside dans le processus de gestion des extensions supprimées sur le VS Code Marketplace, permettant la réutilisation des noms.

**Recommandations :**

*   Les organisations et les développeurs doivent adopter des pratiques de développement sécurisées.
*   Il est crucial de surveiller activement les écosystèmes open-source pour détecter les menaces à la chaîne d'approvisionnement logicielle.
*   Une visibilité sur l'ensemble de la chaîne d'approvisionnement logicielle, associée à une analyse automatisée rigoureuse et une source unique de vérité pour les composants logiciels, est essentielle.

---
[Source](https://thehackernews.com/2025/08/researchers-find-vs-code-flaw-allowing.html){:target="_blank"}
