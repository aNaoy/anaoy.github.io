---
title: 'Alleged TeamPCP Hackers Charged in Australia Over Major Supply Chain Attacks'
date: 2026-08-27
permalink: /posts/2026/08/27/alleged-teampcp-hackers-charged-in-australia-over-major-supply-chain-attacks/
tags:
- veille-cyber
- hackernews
---
### Démantèlement du groupe cybercriminel TeamPCP en Australie

La Police Fédérale Australienne (AFP) a arrêté et inculpé deux hommes, âgés de 21 et 23 ans, pour leur implication au sein du groupe **TeamPCP**. Ce collectif est responsable d'une vaste campagne d'attaques sur la chaîne d'approvisionnement logicielle (supply chain) menée en mars 2026, ciblant notamment les outils *Trivy*, *Checkmarx KICS* et la passerelle AI *LiteLLM*.

**Points clés :**
* **Mode opératoire :** Le groupe dérobait des identifiants de publication sur des projets open source de confiance pour injecter des versions corrompues de logiciels via les canaux officiels (GitHub Actions, Docker Hub, npm, PyPI, OpenVSX).
* **Impact mondial :** L'attaque a potentiellement compromis plus de 1 000 organisations, entraînant le vol de plus de 500 000 identifiants et l'exfiltration d'au moins 300 Go de données.
* **Persistance :** Les infrastructures du groupe sont actives depuis 2020 (anciennement liées aux activités *TA-NATALSTATUS* et *IronErn*).
* **Répercussions :** Les données exfiltrées constituent un risque persistant, les acteurs malveillants pouvant exploiter les secrets volés longtemps après l'incident initial.

**Vulnérabilités :**
Bien qu'aucune CVE spécifique ne soit citée pour le groupe lui-même, l'attaque a exploité :
* Le manque de verrouillage des versions dans les pipelines CI/CD (ex: installation de *Trivy* sans épinglage de version).
* L'utilisation de jetons de publication (tokens) exposés ou compromis dans les chaînes d'intégration continue.
* La confiance aveugle envers les dépendances logicielles tierces.

**Recommandations :**
* **Rotation des secrets :** Renouveler immédiatement tous les secrets CI/CD, jetons de publication et identifiants cloud accessibles durant les périodes d'exposition.
* **Sécurisation des pipelines :** Épingler systématiquement les workflows GitHub Actions et autres outils CI/CD à des **empreintes de commit (SHA hashes)** vérifiées, plutôt qu'à des tags de version flottants.
* **Audit de sécurité :** Rechercher la présence des dépôts nommés `tpcp-docs` ou `docs-tpcp` au sein de l'infrastructure, identifiés par le FBI comme des marqueurs de compromission.
* **Surveillance :** Considérer toutes les données et accès exposés lors de cette campagne comme définitivement compromis.

---
[Source](https://thehackernews.com/2026/08/alleged-teampcp-hackers-charged-in.html){:target="_blank"}
