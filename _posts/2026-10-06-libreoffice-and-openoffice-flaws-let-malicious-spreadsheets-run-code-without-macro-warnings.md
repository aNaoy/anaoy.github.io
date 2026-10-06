---
title: 'LibreOffice and OpenOffice Flaws Let Malicious Spreadsheets Run Code Without Macro Warnings'
date: 2026-10-06
permalink: /posts/2026/10/06/libreoffice-and-openoffice-flaws-let-malicious-spreadsheets-run-code-without-macro-warnings/
tags:
- veille-cyber
- hackernews
---
### Exécution de code arbitraire via LibreOffice et OpenOffice

Une vulnérabilité critique a été identifiée dans LibreOffice et Apache OpenOffice, permettant à un attaquant d'exécuter du code malveillant dès l'ouverture d'un fichier tableur (Calc), sans aucune alerte de sécurité préalable. Cette faille repose sur le détournement des fonctionnalités de mise à jour automatique des données externes ("database ranges") couplées à l'utilisation de pilotes Java (JDBC).

**Points clés :**
*   **Mécanisme d'attaque :** Le fichier malveillant est configuré pour télécharger un fichier de base de données (ODB) distant contenant un pilote JDBC. Le logiciel télécharge et exécute automatiquement ce fichier JAR malveillant via le support Java, contournant ainsi les mécanismes de protection habituels contre les macros.
*   **Conditions :** L'attaque nécessite que le support Java soit activé dans les paramètres du logiciel.
*   **Impact :** Exécution arbitraire de code sur Windows et Linux.

**Vulnérabilités :**
*   **LibreOffice :** CVE-2026-63277
*   **Apache OpenOffice :** CVE-2026-59265

**Recommandations :**
*   **LibreOffice :** Mettre à jour vers les versions 26.2.5 ou 26.8.0 minimum pour bénéficier du correctif.
*   **Apache OpenOffice :** Étant donné qu'aucun correctif n'est encore disponible (attendu pour la version 4.1.17), il est fortement recommandé de **désactiver le support Java** dans les paramètres du logiciel et de s'abstenir d'ouvrir des fichiers tableurs provenant de sources non fiables.

---
[Source](https://thehackernews.com/2026/10/libreoffice-and-openoffice-flaws-let.html){:target="_blank"}
