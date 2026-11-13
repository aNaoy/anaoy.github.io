---
title: 'Policy and Disclosure: 2026 Edition'
date: 2026-11-13
permalink: /posts/2026/11/13/policy-and-disclosure-2026-edition/
tags:
- veille-cyber
- zerodaysfans
---
### Évolution de la politique de divulgation de Project Zero

L'avènement de l'IA générative a radicalement transformé le paysage des menaces : les attaquants découvrent et exploitent les vulnérabilités plus rapidement, rendant les délais de divulgation actuels (90 jours + 30 jours de « soak time ») inadaptés. La réduction du temps entre la publication d'un correctif et son exploitation réelle impose aux éditeurs une réactivité accrue.

**Points clés :**
* **Obsolescence du délai de grâce :** Les périodes de « soak time » (temps de latence pour le déploiement) sont jugées contre-productives, car elles offrent un faux sentiment de sécurité alors que les attaquants peuvent rétro-concevoir les correctifs presque instantanément.
* **Simplification et automatisation :** La nouvelle politique supprime la plupart des cas particuliers (négociations, délais de grâce) pour permettre une automatisation des processus de divulgation.
* **Transition progressive :** Le passage à des délais plus courts s'étalera sur plusieurs années pour permettre aux éditeurs d'adapter leurs infrastructures.
* **Indépendance vis-à-vis de la sévérité :** Désormais, les délais s'appliquent uniformément, indépendamment de la gravité de la faille, car la probabilité de découverte par un attaquant ne dépend pas de la criticité du bug.

**Nouvelle politique « Full X » :**
* **Immédiat :** Passage à « Full 90 » (divulgation 90 jours après signalement).
* **Au 2 février 2027 :** Passage à « Full 60 ».
* **Au 3 janvier 2028 :** Passage à « Full 30 ».

**Exceptions à la règle :**
* Vulnérabilités déjà exploitées activement (*In-the-wild*).
* Vulnérabilités ayant déjà fait l'objet d'une divulgation publique par des tiers.
* Demande explicite de l'éditeur.

**Recommandations pour les éditeurs :**
* **Réduire le « patch gap » :** Prioriser la réduction du temps entre la disponibilité d'un correctif et son installation effective par l'utilisateur.
* **Stratégies alternatives :** En cas d'impossibilité de patch immédiat (notamment sur le matériel), envisager des stratégies de remédiation autres que le correctif logiciel (ex: désactivation temporaire de chemins de code vulnérables).
* **Préparation à la divulgation :** Améliorer les capacités internes de réponse pour s'aligner sur des délais de remédiation de plus en plus courts.

---
[Source](https://projectzero.google/2026/11/disclosure-policy.html){:target="_blank"}
