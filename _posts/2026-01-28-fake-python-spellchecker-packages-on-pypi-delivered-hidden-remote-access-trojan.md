---
title: 'Fake Python Spellchecker Packages on PyPI Delivered Hidden Remote Access Trojan'
date: 2026-01-28
permalink: /posts/2026/01/28/fake-python-spellchecker-packages-on-pypi-delivered-hidden-remote-access-trojan/
tags:
- veille-cyber
- hackernews
---
### Fausses bibliothèques Python sur PyPI déploient un cheval de Troie d'accès à distance

Des chercheurs en cybersécurité ont identifié deux paquets malveillants sur le dépôt Python Package Index (PyPI), qui se présentaient comme des correcteurs orthographiques mais contenaient en réalité un cheval de Troie d'accès à distance (RAT). Les paquets, nommés `spellcheckerpy` et `spellcheckpy`, ont été téléchargés un peu plus d'un millier de fois avant d'être retirés.

Le code malveillant était caché dans un fichier de dictionnaire basque (`resources/eu.json.gz`) sous forme de charge utile encodée en Base64. Cette charge utile téléchargeait un RAT Python complet. Les premières versions des paquets étaient inactives, mais la version 1.2.0 de `spellcheckpy`, publiée le 21 janvier 2026, a activé l'exécution du code malveillant lors de l'importation du module `SpellChecker`. L'attaquant utilisait une adresse IP associée à un fournisseur d'hébergement ayant des antécédents de services à des groupes étatiques.

Ce n'est pas la première fois que de faux outils de correction orthographique Python sont découverts sur PyPI, suggérant que la même menace pourrait être à l'origine de ces campagnes.

**Points clés :**

*   Découverte de deux paquets malveillants (`spellcheckerpy`, `spellcheckpy`) sur PyPI se faisant passer pour des correcteurs orthographiques.
*   Ces paquets contenaient un cheval de Troie d'accès à distance (RAT) Python.
*   Le code malveillant était caché dans un fichier de dictionnaire basque et activé lors de l'importation d'une classe spécifique.
*   Des campagnes similaires utilisant de faux correcteurs orthographiques avaient déjà été observées.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée pour les bibliothèques elles-mêmes, mais l'exploitation repose sur la confiance accordée aux paquets disponibles sur des dépôts publics et sur l'importation de code provenant de sources potentiellement non fiables.

**Recommandations :**

*   Être vigilant quant à l'installation de paquets tiers, même s'ils semblent bénins ou proviennent de dépôts officiels.
*   Vérifier la réputation et l'activité récente des paquets avant de les intégrer dans des projets.
*   Mettre en place des outils de sécurité pour la chaîne d'approvisionnement logicielle afin de détecter les paquets malveillants.

---
[Source](https://thehackernews.com/2026/01/fake-python-spellchecker-packages-on.html){:target="_blank"}
