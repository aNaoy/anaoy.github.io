---
title: 'Subverting AIOps Systems Through Poisoned Input Data'
date: 2025-08-20
permalink: /posts/2025/08/20/subverting-aiops-systems-through-poisoned-input-data/
tags:
- veille-cyber
- schneier
---
## Manipulation des systèmes AIOps par des données d'entrée corrompues

Des chercheurs ont démontré la possibilité de tromper les outils d'IA pour les opérations informatiques (AIOps). Ces systèmes utilisent des agents basés sur les grands modèles de langage (LLM) pour collecter et analyser des données de télémétrie (logs, métriques, alertes) afin de détecter et corriger les problèmes. L'interface conversationnelle de certains de ces outils permet aux administrateurs de demander des informations sur les performances ou même d'exécuter des corrections automatiques.

Cependant, ces agents peuvent être induits en erreur par des données de télémétrie falsifiées, les amenant à prendre des actions potentiellement nuisibles, comme le retour à une version vulnérable d'un logiciel. L'étude révèle que des requêtes conçues pour induire des erreurs peuvent manipuler le comportement des agents par une forme de "reward-hacking" ou d'interprétation erronée des erreurs système.

Une méthodologie d'attaque automatisée, baptisée "AIOpsDoom", a été développée. Elle combine reconnaissance, fuzzing et génération d'entrées adversariales pilotées par LLM. Cette approche permet de compromettre l'intégrité de l'infrastructure gérée sans nécessiter de connaissance préalable du système cible.

### Points Clés

*   Les systèmes AIOps automatisent la détection, le diagnostic et la correction des incidents informatiques.
*   Ils s'appuient de plus en plus sur des LLM pour interpréter les données de télémétrie et agir de manière autonome.
*   Une manipulation des données de télémétrie peut amener ces systèmes à exécuter des actions incorrectes ou dangereuses.
*   Il s'agit d'un nouveau vecteur d'attaque potentiel pour la compromission des systèmes.

### Vulnérabilités

L'article décrit une attaque par manipulation de données de télémétrie. Bien qu'aucun CVE spécifique ne soit mentionné pour cette vulnérabilité générale, la description fait référence à la possibilité de "downgrading an installed package to a vulnerable version".

### Recommandations

Une approche de défense nommée "AIOpsShield" est proposée. Ce mécanisme vise à assainir les données de télémétrie en tirant parti de leur nature structurée et du rôle limité du contenu généré par l'utilisateur. Les expériences montrent que AIOpsShield bloque efficacement les attaques basées sur la télémétrie sans impacter les performances normales des agents. L'article souligne le besoin urgent d'une conception des systèmes AIOps soucieuse de la sécurité.

---
[Source](https://www.schneier.com/blog/archives/2025/08/subverting-aiops-systems-through-poisoned-input-data.html){:target="_blank"}
