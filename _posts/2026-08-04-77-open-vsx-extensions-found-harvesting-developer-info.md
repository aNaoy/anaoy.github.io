---
title: '77 Open VSX extensions found harvesting developer info'
date: 2026-08-04
permalink: /posts/2026/08/04/77-open-vsx-extensions-found-harvesting-developer-info/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de malwares "Evil Twin" sur Open VSX

Soixante-dix-sept extensions malveillantes ont été identifiées sur la place de marché Open VSX entre fin juillet et début août 2026. Ces extensions usurpaient l'identité d'outils de développement légitimes pour exfiltrer des données système et des métadonnées de développement vers un domaine centralisé (`mangorbit.com`).

**Points clés :**
* **Mode opératoire :** Les attaquants ont publié des extensions portant les noms et descriptions d'outils reconnus (ex: AMD, Azure, Salesforce), mais via des comptes tiers.
* **Volume de données :** 58 extensions se limitaient à des données système de base, tandis que 19 autres effectuaient une reconnaissance approfondie.
* **Informations exfiltrées :** Identifiants système, noms d'hôte, chemins de fichiers, configuration Git (branches, dépôts), et métadonnées liées aux environnements CI/CD (GitHub, GitLab, etc.).
* **Absence d'accès direct :** Les outils n'ont pas accédé au code source, aux identifiants, aux jetons d'authentification ou aux clés SSH.
* **Persistance :** Les extensions tentaient de communiquer avec leurs serveurs pendant sept jours et utilisaient des mécanismes de secours DNS pour contourner le blocage d'URL.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, car il s'agit d'une attaque par ingénierie sociale exploitant la confiance dans le dépôt Open VSX. La vulnérabilité réside dans le processus de publication et de validation des extensions.

**Recommandations :**
* **Suppression manuelle :** Désinstaller immédiatement toute extension suspecte des environnements de développement.
* **Filtrage réseau :** Bloquer tout trafic sortant vers le domaine `mangorbit.com` et ses sous-domaines.
* **Audit :** Vérifier les fichiers de configuration de l'espace de travail et les identifiants d'extensions installées en les croisant avec la liste fournie dans le rapport de Manifold Security.
* **Vigilance :** Privilégier l'installation d'extensions dont l'éditeur est vérifié et être attentif aux numéros de version suspects (ex: 0.0.1).

---
[Source](https://www.bleepingcomputer.com/news/security/77-open-vsx-extensions-found-harvesting-developer-info/){:target="_blank"}
