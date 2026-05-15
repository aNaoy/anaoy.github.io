---
title: 'OpenAI confirms security breach in TanStack supply chain attack'
date: 2026-05-15
permalink: /posts/2026/05/15/openai-confirms-security-breach-in-tanstack-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement OpenAI : L'attaque "Mini Shai-Hulud"

OpenAI a été victime d'une intrusion via l'attaque sur la chaîne d'approvisionnement "Mini Shai-Hulud", orchestrée par le groupe TeamPCP. Deux postes de travail d'employés ont été compromis, permettant un accès limité à certains dépôts de code source interne et à des identifiants. Aucun système de production, donnée client ou propriété intellectuelle n'a été exposé.

**Points clés :**
* **Méthode :** Les attaquants ont injecté du code malveillant dans des mises à jour légitimes de paquets npm et PyPI (notamment TanStack), utilisant les processus de publication officiels.
* **Conséquences :** Vol d'identifiants (tokens GitHub, AWS, clés SSH, etc.) et exposition de certificats de signature de code.
* **Propagation :** Le logiciel malveillant assure sa persistance en modifiant des tâches VS Code et des hooks Claude Code, et utilise les accès volés pour infecter d'autres projets.
* **Impact spécifique :** Bien qu'aucune utilisation malveillante des certificats n'ait été détectée, OpenAI a procédé à leur renouvellement par précaution.

**Vulnérabilités :**
* Exploitation des faiblesses dans les configurations CI/CD et les workflows GitHub Actions.
* Absence de sécurisation suffisante des tokens dans la mémoire des systèmes des développeurs.
* *Note : Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'une campagne de compromission de chaîne d'approvisionnement (Supply Chain Attack) via des accès légitimes détournés.*

**Recommandations :**
* **Utilisateurs macOS :** Mettre à jour les applications de bureau OpenAI avant le 12 juin 2026 pour éviter les problèmes liés à la révocation des anciens certificats.
* **Développeurs et entreprises :**
    * Renforcer la sécurité des pipelines CI/CD et surveiller étroitement les workflows automatisés.
    * Révoquer et renouveler systématiquement tous les jetons, secrets et clés d'accès en cas de compromission d'un poste de développement.
    * Auditer les dépendances open-source et les processus de publication pour détecter des injections anormales dans les paquets.
    * Isoler les systèmes de développement des environnements de production critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/openai-confirms-security-breach-in-tanstack-supply-chain-attack/){:target="_blank"}
