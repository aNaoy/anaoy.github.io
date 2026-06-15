---
title: 'Evil MSI Background: BASE64 Statistical Analysis, (Mon, Jun 15th)'
date: 2026-06-15
permalink: /posts/2026/06/15/evil-msi-background-base64-statistical-analysis-mon-jun-15th/
tags:
- veille-cyber
- sans-isc
---
### Analyse forensique : Détection de charges malveillantes dissimulées via encodage personnalisé

Cette analyse porte sur l'identification d'un fichier exécutable (PE) malveillant dissimulé au sein d'une image JPEG, technique utilisée pour masquer des charges utiles dans des installateurs MSI. L'étude démontre comment les outils d'analyse statistique peuvent révéler des obfuscations complexes.

**Points clés :**
* **Dissimulation :** Le fichier JPEG contient une charge utile de près d'un million de caractères encodés.
* **Obfuscation :** L'attaquant utilise un encodage personnalisé basé sur le BASE64, mais avec une modification structurelle : la chaîne de caractères est inversée.
* **Indicateur technique :** La présence de la séquence "TVq" (le marqueur "MZ" inversé) à la fin de la chaîne est un indicateur clé de la présence d'un exécutable Windows (PE).
* **Méthodologie :** L'utilisation d'outils d'analyse statistique (`byte-stats.py`) permet de confirmer la nature des données avant même de réussir à les décoder, en isolant les fréquences anormales de caractères.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car il s'agit d'une technique de **stéganographie et d'obfuscation de code** visant à contourner les solutions de détection statique par signature.

**Recommandations :**
* **Analyse comportementale :** Ne pas se fier uniquement aux signatures de fichiers (hash). Les outils de sécurité doivent inspecter le contenu des fichiers images pour détecter des anomalies statistiques.
* **Décodage multi-niveaux :** En cas de suspicion, tester systématiquement l'inversion des chaînes de caractères (reverse) ou des substitutions personnalisées d'alphabets BASE64 lors du processus de "carving".
* **Veille sur les outils :** Utiliser des outils d'analyse de données (comme la suite Didier Stevens) capables de calculer les statistiques de fréquence de caractères pour identifier des encodages non standards.

---
[Source](https://isc.sans.edu/diary/rss/33072){:target="_blank"}
