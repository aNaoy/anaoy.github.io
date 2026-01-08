---
title: 'New GoBruteforcer attack wave targets crypto, blockchain projects'
date: 2026-01-08
permalink: /posts/2026/01/08/new-gobruteforcer-attack-wave-targets-crypto-blockchain-projects/
tags:
- veille-cyber
- bleepingcomp
---
**Vague d'attaques GoBruteforcer : Menace sur les projets crypto et blockchain**

Une nouvelle campagne de malware, GoBruteforcer (également connu sous le nom de GoBrut), exploite des serveurs exposés, en particulier ceux configurés à l'aide d'exemples générés par IA, pour cibler les bases de données de projets de cryptomonnaies et de blockchain. Ce botnet, développé en Golang, vise principalement les services FTP, MySQL, PostgreSQL et phpMyAdmin mal sécurisés.

Les chercheurs estiment que plus de 50 000 serveurs connectés à Internet pourraient être vulnérables. L'infection initiale se fait souvent via des serveurs FTP tournant sous XAMPP, exploitant des identifiants par défaut faibles. Une fois l'accès obtenu, les attaquants déploient un "web shell" pour ensuite télécharger un bot IRC et le module de brute-force. Ce dernier scanne des adresses IP publiques aléatoires pour tenter de deviner les identifiants de connexion.

Les configurations récentes, potentiellement influencées par les instructions générées par les grands modèles linguistiques (LLM), introduisent des noms d'utilisateur par défaut prévisibles tels que "appuser", "myuser" et "operator", qui sont ensuite ciblés par des attaques par pulvérisation de mots de passe. L'utilisation continue de piles logicielles obsolètes comme XAMPP, livrées avec des identifiants par défaut, aggrave la situation.

Des cas récents ont montré que les serveurs compromis sont utilisés pour scanner et cibler des portefeuilles TRON et Binance Smart Chain (BSC) afin de drainer les fonds.

**Points clés :**

*   **Cible :** Bases de données de projets crypto et blockchain sur serveurs exposés.
*   **Vecteur d'attaque :** Botnet GoBruteforcer visant les services FTP, MySQL, PostgreSQL, phpMyAdmin.
*   **Méthode d'infection :** Exploitation de configurations faibles (par défaut ou générées par IA), identifiants par défaut, XAMPP obsolète, puis brute-force.
*   **Objectif :** Accès aux données sensibles, vol de cryptomonnaies via des scans de portefeuilles automatisés.
*   **Prévalence :** Plus de 50 000 serveurs potentiellement vulnérables.

**Vulnérabilités :**

*   Utilisation d'identifiants par défaut faibles pour les services FTP, MySQL, PostgreSQL, phpMyAdmin.
*   Serveurs tournant avec des configurations potentiellement influencées par des exemples générés par IA, introduisant des noms d'utilisateur prévisibles.
*   Utilisation de piles logicielles obsolètes comme XAMPP avec des services FTP ouverts.

**Recommandations :**

*   Éviter l'utilisation de guides de déploiement générés par IA.
*   Utiliser des noms d'utilisateur non par défaut et des mots de passe forts et uniques.
*   Vérifier et sécuriser les services FTP, phpMyAdmin, MySQL et PostgreSQL exposés sur Internet.
*   Remplacer les piles logicielles obsolètes par des alternatives plus sécurisées.

---
[Source](https://www.bleepingcomputer.com/news/security/new-gobruteforcer-attack-wave-targets-crypto-blockchain-projects/){:target="_blank"}
