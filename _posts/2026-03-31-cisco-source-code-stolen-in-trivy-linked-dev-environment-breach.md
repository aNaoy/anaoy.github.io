---
title: 'Cisco source code stolen in Trivy-linked dev environment breach'
date: 2026-03-31
permalink: /posts/2026/03/31/cisco-source-code-stolen-in-trivy-linked-dev-environment-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de la chaîne d'approvisionnement : Cisco victime d'un vol de code source

Cisco a subi une intrusion majeure dans son environnement de développement suite à une attaque par chaîne d'approvisionnement ciblant l'outil de scan de vulnérabilités **Trivy**. Des attaquants ont exploité un plugin GitHub Actions malveillant pour exfiltrer des identifiants, accéder aux environnements CI/CD et cloner plus de 300 dépôts GitHub. Le vol inclut du code source propriétaire, des projets liés à l'IA, ainsi que des données appartenant à des clients (banques, agences gouvernementales). Des clés AWS ont également été dérobées pour mener des activités non autorisées.

**Points clés :**
*   **Acteurs de la menace :** Le groupe "TeamPCP", spécialisé dans les attaques de chaîne d'approvisionnement (compromissions précédentes : LiteLLM, Checkmarx KICS, NPM, PyPi).
*   **Impact :** Compromission de postes de travail de développement, exfiltration de code source, utilisation malveillante de comptes AWS et exposition potentielle de données clients.
*   **Infection initiale :** Utilisation d'un malware de type "infostealer" (TeamPCP Cloud Stealer) diffusé via des pipelines CI/CD compromis.

**Vulnérabilités :**
*   L'attaque repose sur des vulnérabilités de confiance dans les dépendances logicielles et les outils tiers (GitHub Actions). Bien qu'aucune CVE spécifique ne soit attribuée à cette intrusion, elle illustre les risques critiques liés aux supply chain attacks ciblant les pipelines de développement.

**Recommandations :**
*   **Rotation des accès :** Procéder à une réinitialisation immédiate et généralisée des identifiants (secrets CI/CD, clés AWS, jetons GitHub).
*   **Isolement et remédiation :** Isoler et réimager systématiquement les machines de développement et les environnements de laboratoire impactés.
*   **Surveillance accrue :** Auditer les logs des pipelines CI/CD pour détecter des activités anormales liées à l'utilisation d'outils tiers.
*   **Gestion des dépendances :** Renforcer les processus de vérification des plugins et outils intégrés aux pipelines, en privilégiant l'épinglage des versions et l'analyse de l'intégrité des flux automatisés.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-source-code-stolen-in-trivy-linked-dev-environment-breach/){:target="_blank"}
