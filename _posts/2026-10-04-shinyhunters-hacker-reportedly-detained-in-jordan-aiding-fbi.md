---
title: 'ShinyHunters hacker reportedly detained in Jordan, aiding FBI'
date: 2026-10-04
permalink: /posts/2026/10/04/shinyhunters-hacker-reportedly-detained-in-jordan-aiding-fbi/
tags:
- veille-cyber
- bleepingcomp
---
### Arrestation d'un membre clé de ShinyHunters et coopération avec le FBI

Un membre influent du groupe de cybercriminels « ShinyHunters », identifié sous le pseudonyme « Rey » (Saif al-Din Khader), a été arrêté en Jordanie. Il collabore désormais activement avec le FBI pour aider les autorités à localiser d'autres membres du réseau d'extorsion. Cette arrestation s'inscrit dans une offensive internationale accrue contre le groupe, notamment après une cyberattaque visant le FBI en septembre, où des données auraient été dérobées via une exploitation supposée de vulnérabilité.

**Points clés :**
* **Coopération sous contrainte :** Khader assiste le FBI en fournissant l'accès à ses appareils électroniques et communications numériques pour identifier ses complices.
* **Mode opératoire du groupe :** ShinyHunters se spécialise dans l'extorsion et le vol de données à grande échelle. Ils ciblent fréquemment les environnements SaaS (Salesforce, etc.) en compromettant des tiers intégrateurs pour récupérer des jetons d'authentification.
* **Perturbations opérationnelles :** Suite à l'arrestation, des sites de fuite de données associés au groupe ont été temporairement hors ligne et les communications avec les médias ont cessé, bien qu'un nouveau site ait été mis en ligne peu après.
* **Antécédents du suspect :** « Rey » est lié à de nombreuses cyberattaques majeures depuis 2025, notamment celles visant Telefónica, Orange et Jaguar Land Rover, souvent en lien avec des groupes comme *HellCat* et *Scattered Lapsus$ Hunters*.

**Vulnérabilités :**
* **Oracle PeopleSoft (Zero-day) :** Utilisée lors de l'attaque présumée contre le FBI pour infiltrer le réseau, puis pour un déplacement latéral vers AWS GovCloud. (Aucune CVE spécifique n'est mentionnée dans l'article).

**Recommandations de sécurité :**
* **Sécurisation des intégrations :** Renforcer la surveillance des accès tiers et des intégrateurs SaaS pour prévenir l'usage frauduleux de jetons d'authentification.
* **Gestion des privilèges :** Appliquer strictement le principe du moindre privilège sur les systèmes internes (Jira, serveurs cloud) afin de limiter l'impact en cas de compromission.
* **Vigilance face aux "InfoStealers" :** Les fuites de logs provenant de malwares de type infostealer étant utilisées pour identifier des acteurs comme Khader, il est crucial de protéger les postes de travail contre ces malwares qui dérobent les sessions actives.

---
[Source](https://www.bleepingcomputer.com/news/security/shinyhunters-hacker-reportedly-detained-in-jordan-aiding-fbi/){:target="_blank"}
