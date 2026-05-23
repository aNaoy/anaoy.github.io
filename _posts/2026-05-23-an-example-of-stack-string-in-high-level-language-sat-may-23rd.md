---
title: 'An Example of Stack String in High Level Language, (Sat, May 23rd)'
date: 2026-05-23
permalink: /posts/2026/05/23/an-example-of-stack-string-in-high-level-language-sat-may-23rd/
tags:
- veille-cyber
- sans-isc
---
### L'obfuscation par "Stack Strings" : Défis et détection

La technique des "stack strings" est une méthode d'obfuscation couramment utilisée par les logiciels malveillants pour contourner la détection statique. Au lieu de stocker des chaînes de caractères (URL, adresses IP, commandes) dans les sections de données standard du binaire, celles-ci sont reconstruites octet par octet directement sur la pile (*stack*) lors de l'exécution.

**Points clés :**
* **Contournement des outils simples :** Les outils d'analyse statique classiques tels que `strings` ou `pestr` sont inefficaces car les chaînes ne sont pas présentes en clair dans le fichier binaire.
* **Complexité d'analyse :** Cette technique force l'analyste à examiner le code assembleur pour identifier des instructions de déplacement (`mov`) successives de valeurs hexadécimales vers la pile.
* **Détection automatisable :** Bien que complexe à repérer manuellement, cette méthode laisse des traces prévisibles au niveau assembleur (séquences répétitives de `mov BYTE PTR`).

**Vulnérabilités :**
* Cet article ne traite pas d'une vulnérabilité logicielle spécifique avec un identifiant CVE, mais expose une **technique d'évasion** utilisée par les attaquants pour dissimuler des indicateurs de compromission (IoC) aux systèmes de sécurité (EDR/antivirus).

**Recommandations :**
* **Utilisation d'outils spécialisés :** Employer des outils d'analyse avancés comme **FLOSS** (FireEye Labs Obfuscated String Solver), conçus pour identifier et extraire automatiquement les chaînes de caractères désobfuscées dynamiquement.
* **Analyse de code automatisée :** Intégrer des scripts d'extraction basés sur l'analyse statique du désassembleur (ex: `objdump` ou Ghidra) pour filtrer les instructions de type `mov` ciblant des adresses de pile contiguës.
* **Reverse engineering rigoureux :** Ne pas se fier uniquement aux chaînes extraites automatiquement et maintenir une veille sur les modèles d'instructions assembleur suspects lors de l'examen de binaires opaques.

---
[Source](https://isc.sans.edu/diary/rss/33008){:target="_blank"}
