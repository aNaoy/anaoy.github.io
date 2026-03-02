---
title: 'Quick Howto: ZIP Files Inside RTF, (Mon, Mar 2nd)'
date: 2026-03-02
permalink: /posts/2026/03/02/quick-howto-zip-files-inside-rtf-mon-mar-2nd/
tags:
- veille-cyber
- sans-isc
---
**Extraction d'URLs depuis des fichiers RTF contenant des archives ZIP**

Une méthode a été développée pour extraire des URLs contenues dans des fichiers RTF qui intègrent des objets OLE. Ces objets peuvent, dans certains cas, cacher des archives ZIP, qui elles-mêmes contiennent des documents (par exemple, au format .docx). La technique précédente d'extraction d'URLs directement depuis les RTF ne fonctionne pas pour ces archives ZIP embarquées.

L'analyse s'appuie sur des scripts Python : `oledump.py` pour inspecter les objets OLE et `zipdump.py` pour traiter spécifiquement le contenu des ZIP. En recherchant la séquence hexadécimale `50 4B 03 04`, qui correspond à l'en-tête d'un fichier ZIP, il devient possible d'identifier et d'extraire ces archives. Une fois le ZIP extrait, les URLs qu'il contient peuvent être récupérées.

**Points Clés :**

*   Les fichiers RTF peuvent contenir des objets OLE.
*   Ces objets OLE peuvent dissimuler des archives ZIP.
*   Les archives ZIP, étant des conteneurs, masquent les URLs qu'elles renferment vis-à-vis des méthodes d'extraction simples sur RTF.
*   Une séquence hexadécimale spécifique (`50 4B 03 04`) permet de détecter les fichiers ZIP intégrés.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est explicitement mentionnée dans cet article. L'article décrit une technique d'analyse pour découvrir du contenu malveillant potentiel caché dans des fichiers RTF et leurs archives ZIP embarquées.

**Recommandations :**

*   Utiliser des outils spécialisés comme `oledump.py` et `zipdump.py` pour analyser le contenu des fichiers RTF potentiellement suspects.
*   Être vigilant quant aux fichiers RTF, car ils peuvent servir de conteneurs pour des archives ZIP et dissimuler des URLs ou des charges utiles malveillantes.
*   Appliquer les techniques décrites pour une investigation plus poussée des fichiers RTF qui pourraient contenir des éléments masqués.

---
[Source](https://isc.sans.edu/diary/rss/32696){:target="_blank"}
