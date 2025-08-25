---
title: 'Reading Location Position Value in Microsoft Word Documents, (Mon, Aug 25th)'
date: 2025-08-25
permalink: /posts/2025/08/25/reading-location-position-value-in-microsoft-word-documents-mon-aug-25th/
tags:
- veille-cyber
- sans-isc
---
### Analyse de la valeur "Position" dans Microsoft Word

L'examen de la valeur "Position" dans le registre Windows révèle comment Microsoft Word enregistre la dernière localisation de lecture d'un document. Cette fonctionnalité, souvent présentée sous forme de suggestion pour reprendre là où l'utilisateur s'est arrêté, repose sur deux composantes principales dans la valeur du registre.

**Points Clés :**

*   **Fonctionnement :** La valeur "Position" dans le registre (`HKEY_CURRENT_USER\Software\Microsoft\Office\<version>\Word\Reading Locations\`) contient deux nombres.
*   **Première Valeur :** Correspond à l'identifiant de paragraphe (`w14:paraId`) trouvé dans le fichier XML interne du document Word. Ce numéro peut changer lorsqu'un nouveau paragraphe est créé (par exemple, en appuyant sur "Entrée"). Il est stocké en format hexadécimal dans le XML et est converti en décimal dans le registre.
*   **Deuxième Valeur :** Représente le nombre de caractères depuis le début du document jusqu'à la première ligne visible à l'écran lorsque le document a été fermé. Cette valeur n'est mise à jour que lorsque la ligne supérieure visible change. L'incrémentation semble correspondre au nombre de caractères sortis de la vue lors du défilement.
*   **Importance de la Deuxième Valeur :** Si seule la deuxième valeur est modifiée pour indiquer une position valide, la fonction de reprise fonctionne, plaçant le curseur à cet emplacement. Cependant, Word ajustera la première valeur pour qu'elle corresponde à la ligne visible.
*   **Importance de la Première Valeur :** Modifier uniquement la première valeur (même si elle est valide) sans changer la seconde n'active pas la fonction de reprise. Elle semble être enregistrée en fonction de l'emplacement visible lors de la fermeture, mais n'est pas le facteur déterminant pour le saut à la dernière localisation.

**Vulnérabilités :**

Aucune vulnérabilité spécifique n'est détaillée dans l'article. L'information concerne plutôt une fonctionnalité interne de Word et son enregistrement dans le registre, potentiellement exploitable pour des analyses forensiques.

**Recommandations :**

*   **Analyse Forensique :** Les informations stockées dans la valeur "Position" peuvent être utilisées dans des analyses forensiques pour déterminer la dernière position de lecture d'un utilisateur dans un document Word. Il est possible de configurer un système de test pour enregistrer ces valeurs dans le registre et d'ouvrir le document correspondant afin de retrouver le point de dernière visualisation.
*   **Automatisation :** Ces données peuvent être exploitées de manière programmatique pour extraire des données de documents Word à partir du point de dernière visualisation, optimisant ainsi les processus d'analyse.

---
[Source](https://isc.sans.edu/diary/rss/32224){:target="_blank"}
