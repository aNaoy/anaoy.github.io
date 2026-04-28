---
title: 'Checkmarx confirms LAPSUS$ hackers leaked its stolen GitHub data'
date: 2026-04-28
permalink: /posts/2026/04/28/checkmarx-confirms-lapsus-hackers-leaked-its-stolen-github-data/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement Checkmarx par le groupe LAPSUS$

Checkmarx a confirmé que le groupe de pirates LAPSUS$ a divulgué des données volées suite à une intrusion dans ses dépôts GitHub privés. L'incident a permis aux attaquants d'injecter du code malveillant dans des outils de sécurité de l'entreprise.

**Points clés :**
* **Vecteur d'attaque :** L'intrusion initiale découle d'une attaque par chaîne d'approvisionnement visant le scanner Trivy (attribuée au groupe TeamPCP), qui a compromis des identifiants utilisés par Checkmarx.
* **Chronologie :** L'accès a été obtenu le 23 mars 2026, permettant l'injection de code malveillant. Le 22 avril, des images Docker et des extensions VSCode/Open VSX corrompues pour l'outil KICS ont été publiées.
* **Impact :** 96 Go de données ont été publiés sur le dark web et en clair. Ces outils malveillants étaient conçus pour exfiltrer des identifiants, des jetons d'accès et des fichiers de configuration.
* **Données clients :** Checkmarx affirme que les données clients ne sont pas stockées sur GitHub et n'auraient, à ce stade, pas été compromises.

**Vulnérabilités :**
* L'incident ne fait pas état d'une vulnérabilité logicielle spécifique (CVE), mais souligne une faille dans la gestion de la **chaîne d'approvisionnement (Supply Chain Attack)**. Le recours à des dépendances tierces compromises (Trivy) a permis l'usurpation d'identifiants légitimes.

**Recommandations :**
* **Audit des accès :** Révoquer immédiatement les identifiants, clés API et jetons (tokens) ayant pu transiter par les dépôts GitHub compromis.
* **Vérification des extensions :** Désinstaller et réinstaller les extensions VSCode/Open VSX et les images Docker liées à KICS à partir de sources vérifiées et sécurisées.
* **Renforcement de la sécurité CI/CD :** Mettre en œuvre une surveillance stricte des pipelines de développement et effectuer un audit régulier des accès tiers et des dépendances logicielles.
* **Surveillance proactive :** Attendre les conclusions de l'enquête forensique en cours pour identifier d'éventuels vecteurs de persistance supplémentaires.

---
[Source](https://www.bleepingcomputer.com/news/security/checkmarx-confirms-lapsus-hackers-leaked-its-stolen-github-data/){:target="_blank"}
