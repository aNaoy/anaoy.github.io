---
title: 'Microsoft: New Windows LNK spoofing issues arent vulnerabilities'
date: 2026-02-13
permalink: /posts/2026/02/13/microsoft-new-windows-lnk-spoofing-issues-arent-vulnerabilities/
tags:
- veille-cyber
- bleepingcomp
---
**Usurpation de raccourcis Windows : une technique trompeuse qui contourne la sécurité**

Des chercheurs en sécurité ont découvert plusieurs méthodes pour manipuler les fichiers de raccourcis LNK de Windows afin de masquer des cibles malveillantes. Ces techniques exploitent des incohérences dans la manière dont l'Explorateur Windows traite les chemins de destination conflictuels au sein de ces fichiers.

**Points clés :**

*   Les fichiers LNK, présents depuis Windows 95, utilisent un format binaire complexe permettant de créer des raccourcis qui affichent un contenu légitime mais exécutent un programme différent.
*   Quatre nouvelles techniques ont été documentées, exploitant notamment l'utilisation de caractères de chemin Windows non conformes ou la manipulation de blocs de données spécifiques comme `EnvironmentVariableDataBlock`.
*   L'une des méthodes les plus efficaces consiste à définir un faux chemin de destination (par exemple, un nom de fichier PDF) dans la fenêtre des propriétés, tout en exécutant en arrière-plan des commandes PowerShell ou d'autres codes malveillants.
*   Ces raccourcis permettent de dissimuler complètement le programme réellement exécuté et les éventuels arguments de ligne de commande, rendant la détection par l'utilisateur très difficile.
*   L'outil "lnk-it-up" a été publié pour générer ces raccourcis LNK et aider à identifier les fichiers potentiellement malveillants.

**Vulnérabilités (avec CVE) :**

Bien que Microsoft considère ces découvertes comme n'étant pas des vulnérabilités répondant à leurs critères de classification immédiate (car nécessitant une interaction utilisateur), elles sont étroitement liées à des techniques déjà exploitées.

*   **CVE-2025-9491 :** Similaire aux nouvelles découvertes, cette vulnérabilité déjà connue permet de masquer des arguments de ligne de commande dans les fichiers LNK via un remplissage excessif d'espaces blancs. Elle a été activement exploitée par de nombreux groupes cybercriminels et parrainés par des États pour des attaques zero-day, notamment pour déployer le RAT PlugX. Microsoft a finalement modifié le traitement des fichiers LNK en juin 2025 pour atténuer cette faille.

**Recommandations :**

*   Microsoft Defender et Smart App Control offrent des protections contre ces menaces.
*   Il est fortement recommandé aux utilisateurs de faire preuve de prudence et d'éviter d'ouvrir des fichiers provenant de sources inconnues.
*   Soyez attentif aux avertissements de sécurité générés par Windows lors de l'ouverture de fichiers .lnk téléchargés, même s'ils peuvent être facilement ignorés.
*   L'outil "lnk-it-up" peut être utilisé pour tester et analyser des fichiers LNK suspects.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-new-windows-lnk-spoofing-issues-arent-vulnerabilities/){:target="_blank"}
