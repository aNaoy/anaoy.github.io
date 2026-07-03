---
title: 'Claude Fable relaunch disappoints users with nerfed performance'
date: 2026-07-03
permalink: /posts/2026/07/03/claude-fable-relaunch-disappoints-users-with-nerfed-performance/
tags:
- veille-cyber
- bleepingcomp
---
### Claude Fable : Entre restrictions d'accès et sur-sécurisation paralysante

Le retour du modèle Claude Fable (version 5) est marqué par une déception générale des utilisateurs, confrontés à une dégradation perçue de ses capacités. Bien que techniquement disponible pour les abonnés, le modèle subit des limitations d'usage sévères et une sensibilité excessive de ses filtres de sécurité.

**Points clés :**
* **Restrictions d'accès :** L'usage est limité à 50 % du quota hebdomadaire, avec une transition complète vers un modèle payant à la consommation prévue pour le 7 juillet.
* **Comportement « nerfé » :** Le modèle bascule fréquemment vers Opus 4.8 sans justification claire, nuisant à l'expérience utilisateur.
* **Sur-sécurisation :** Les mécanismes de garde-fous (guardrails) d'Anthropic sont jugés trop stricts. Des termes anodins liés au développement système (ex: "sécurité", "vulnérable", "pointeurs", "hook") déclenchent systématiquement des blocages ou des rétrogradations vers des modèles moins performants.
* **Origine du problème :** Il ne s'agirait pas d'une dégradation du modèle lui-même, mais d'une application trop prudente de nouvelles mesures de sécurité par Anthropic, générant de nombreux faux positifs.

**Vulnérabilités :**
* Aucune CVE identifiée. Le problème relève d'une problématique de **fiabilité opérationnelle** et de **faux positifs** dans le filtrage de contenu, et non d'une faille de sécurité logicielle exploitable.

**Recommandations :**
* **Pour les développeurs :** Anticiper les blocages lors de travaux sur du code système sensible (C, Rust, gestion mémoire) en préparant des alternatives ou en ajustant la formulation des prompts.
* **Pour Anthropic :** Il est nécessaire d'affiner les seuils de sensibilité des garde-fous pour réduire les faux positifs qui entravent l'utilisabilité réelle du modèle, tout en communiquant de manière transparente sur les causes des basculements vers Opus 4.8.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/claude-fable-relaunch-disappoints-users-with-nerfed-performance/){:target="_blank"}
