---
title: 'Prompt Injection Via Road Signs'
date: 2026-02-11
permalink: /posts/2026/02/11/prompt-injection-via-road-signs/
tags:
- veille-cyber
- schneier
---
### Vol de Commandes dans l'IA Embarquée via des Indices Visuels

Une nouvelle classe d'attaques, nommée CHAI (Command Hijacking against embodied AI), exploite les capacités d'interprétation multimodale des grands modèles visuels-linguistiques (LVLM). Ces modèles sont conçus pour permettre aux systèmes d'IA embarquée, tels que les véhicules autonomes, de raisonner et de s'adapter à des situations inédites en combinant perception et action.

L'approche CHAI consiste à intégrer des instructions trompeuses en langage naturel dans les entrées visuelles, comme de faux panneaux de signalisation. En explorant systématiquement l'espace des "tokens" (unités de texte), les attaquants peuvent construire un répertoire de phrases d'attaque et générer des "prompts" visuels capables de manipuler le comportement des IA.

Les expérimentations ont été menées sur des agents d'IA embarquée dans des scénarios de vol de drones, de conduite autonome et de suivi d'objets aériens, y compris sur un véhicule robotisé réel. Les résultats démontrent que CHAI surpasse les méthodes d'attaque existantes.

Cette recherche met en évidence le besoin urgent de développer des défenses qui vont au-delà des techniques traditionnelles de robustesse face aux attaques adversariales, en particulier pour les systèmes d'IA embarquée de nouvelle génération qui s'appuient sur le raisonnement sémantique et multimodal.

**Points Clés :**

*   Introduction de CHAI, une nouvelle méthode d'attaque contre les IA embarquées.
*   Exploitation des capacités multimodales des grands modèles visuels-linguistiques (LVLM).
*   Utilisation d'indices visuels trompeurs (ex: faux panneaux) pour manipuler les instructions.
*   Démonstration de l'efficacité sur plusieurs scénarios d'IA embarquée.

**Vulnérabilités :**

*   La recherche ne mentionne pas de CVE spécifiques pour ces vulnérabilités, car elle introduit une nouvelle classe d'attaques basées sur des principes généraux d'injection de prompt dans un contexte multimodal. Les vulnérabilités exploitées sont inhérentes à la manière dont les LVLM interprètent et agissent sur des instructions visuelles et textuelles combinées.

**Recommandations :**

*   Développer des mécanismes de défense robustes qui anticipent les attaques par injection de prompt dans les données multimodales.
*   Explorer des solutions au-delà de la seule robustesse adversariale traditionnelle.

---
[Source](https://www.schneier.com/blog/archives/2026/02/prompt-injection-via-road-signs.html){:target="_blank"}
