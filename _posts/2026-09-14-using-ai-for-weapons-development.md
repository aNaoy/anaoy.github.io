---
title: 'Using AI for Weapons Development'
date: 2026-09-14
permalink: /posts/2026/09/14/using-ai-for-weapons-development/
tags:
- veille-cyber
- schneier
---
### L'IA au service de la prolifération d'armements

Anthropic a révélé qu'une cellule de cyberacteurs basée au Yémen a exploité son modèle Claude pour développer des systèmes d'armement sophistiqués, notamment des missiles balistiques et des fusées guidées. En utilisant l'outil "Claude Code", ces acteurs ont automatisé la création de logiciels de guidage, de navigation et de contrôle (GNC) en déléguant des tâches complexes à plusieurs instances de l'IA agissant comme une équipe d'ingénieurs.

**Points clés :**
* **Démocratisation de l'expertise :** L'utilisation de l'IA a permis de pallier un manque de compétences techniques humaines pour concevoir des systèmes de stabilisation de vol complexes.
* **Méthodes de contournement :** Les attaquants ont réussi à tromper les garde-fous d'Anthropic en morcelant leurs requêtes sur plusieurs sessions et en dissimulant la finalité militaire de leurs projets.
* **Boucle de rétroaction :** Les acteurs ont utilisé l'IA pour analyser les échecs de leurs essais en vol afin d'ajuster itérativement leur code et leurs paramètres de contrôle.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais met en évidence une vulnérabilité conceptuelle : la capacité des modèles de langage à assister la création de technologies à double usage (civil/militaire) lorsque les mesures de sécurité sont contournées par une segmentation des tâches.

**Recommandations :**
* **Renforcement des filtres contextuels :** Améliorer la détection des intentions malveillantes en analysant la cohérence des requêtes sur le long terme plutôt que de se limiter à l'analyse de sessions isolées.
* **Surveillance des usages industriels :** Accroître la vigilance sur les requêtes impliquant des bibliothèques de code liées à l'aérospatiale, aux systèmes de guidage (GNC) ou aux technologies de défense.
* **Transparence et signalement :** Maintenir une collaboration étroite entre les développeurs d'IA et les autorités de régulation pour identifier les modèles de comportement typiques de la recherche militaire clandestine.

---
[Source](https://www.schneier.com/blog/archives/2026/09/using-ai-for-weapons-development.html){:target="_blank"}
