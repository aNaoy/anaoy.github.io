---
title: 'Fake Paysafe, Skrill SDKs on NPM and PyPi steal credentials'
date: 2026-07-09
permalink: /posts/2026/07/09/fake-paysafe-skrill-sdks-on-npm-and-pypi-steal-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de malwares visant les développeurs via des SDK de paiement contrefaits

Une campagne malveillante a infiltré les registres NPM et PyPI en publiant 17 bibliothèques usurpant l'identité de services de paiement légitimes (Paysafe, Skrill, Neteller). Ces packages frauduleux sont conçus pour exfiltrer des données sensibles directement depuis les environnements de développement des utilisateurs.

**Points clés :**
* **Cible :** Développeurs intégrant des solutions de paiement dans des applications e-commerce ou financières.
* **Méthode :** Utilisation de packages contrefaits (typosquatting) qui imitent les API officielles tout en retournant de fausses réponses de succès.
* **Exfiltration :** Le code malveillant recherche et envoie à un serveur C2 (hébergé sur AWS) des clés API Paysafe, des clés AWS, des tokens GitHub/NPM, ainsi que des informations système.
* **Mécanismes de dissimulation :** Les packages intègrent des fonctions anti-analyse bloquant l'exécution s'ils détectent un environnement virtualisé (sandbox) ou une configuration matérielle limitée.
* **Vulnérabilités :** Aucune CVE spécifique n'est associée, car il s'agit d'une attaque par "supply chain" utilisant des paquets malveillants injectés directement dans les registres open-source.

**Recommandations :**
* **Audit immédiat :** Vérifier les arbres de dépendances des projets pour identifier l'un des 17 packages listés (ex: `paysafe-checkout`, `skrill-payments`, `paysafe-api`, etc.).
* **Rotation des secrets :** En cas d'installation avérée, révoquer et régénérer immédiatement tous les secrets (clés API, tokens GitHub/NPM, identifiants AWS) présents sur les machines concernées.
* **Surveillance CI/CD :** Analyser les logs des systèmes d'intégration continue à la recherche de toute interaction entre les packages suspects et des variables d'environnement critiques comme `PAYSAFE_API_KEY`.
* **Filtrage :** Bloquer les requêtes vers ces noms de paquets au niveau des proxys de registre (registry proxies) pour empêcher toute installation accidentelle future.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-paysafe-skrill-sdks-on-npm-and-pypi-steal-credentials/){:target="_blank"}
