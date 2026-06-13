---
title: 'US Gov asks Anthropic to ban foreign national access to Fable, Mythos'
date: 2026-06-13
permalink: /posts/2026/06/13/us-gov-asks-anthropic-to-ban-foreign-national-access-to-fable-mythos/
tags:
- veille-cyber
- bleepingcomp
---
### Restriction des modèles d'IA Anthropic pour des raisons de sécurité nationale

Anthropic a suspendu l'accès mondial à ses modèles d'IA les plus avancés, **Fable 5** et **Mythos 5**, suite à une directive de contrôle des exportations émise par le gouvernement américain. Cette décision fait suite à des préoccupations de sécurité nationale concernant l'accès à ces technologies par des ressortissants étrangers, y compris au sein même du personnel d'Anthropic.

**Points clés :**
* **Portée de la mesure :** Bien que la directive vise les ressortissants étrangers, les contraintes techniques imposent à Anthropic de bloquer l'accès à ces deux modèles pour l'ensemble des utilisateurs, partout dans le monde. Les autres modèles, comme Claude Opus 4.8, restent accessibles.
* **Contexte de la faille :** Le gouvernement s'inquiète d'un potentiel "jailbreak" permettant au modèle d'analyser un code source pour identifier et corriger des failles de sécurité.
* **Position d'Anthropic :** L'entreprise conteste la gravité de la vulnérabilité signalée, la qualifiant de "mineure" et comparable aux capacités déjà présentes dans d'autres modèles du marché. Elle juge cette mesure de rappel disproportionnée et préjudiciable au déploiement de nouvelles technologies.

**Vulnérabilités :**
* Aucune CVE n'est associée à cet événement. Il s'agit d'une vulnérabilité logique liée à la capacité du modèle à effectuer de l'analyse de code automatisée (assistance à la découverte de vulnérabilités logicielles).

**Recommandations :**
* **Pour les utilisateurs :** Les développeurs et clients utilisant Fable 5 ou Mythos 5 doivent migrer vers des modèles alternatifs (tels que Claude Opus 4.8) pour assurer la continuité de leurs services.
* **Pour les entreprises :** Il est conseillé de surveiller les communications d'Anthropic pour obtenir des mises à jour sur la résolution du conflit et le rétablissement potentiel des services, tout en évaluant la dépendance aux modèles "frontier" vis-à-vis des futures régulations étatiques.

---
[Source](https://www.bleepingcomputer.com/news/security/us-gov-asks-anthropic-to-ban-foreign-national-access-to-fable-mythos/){:target="_blank"}
