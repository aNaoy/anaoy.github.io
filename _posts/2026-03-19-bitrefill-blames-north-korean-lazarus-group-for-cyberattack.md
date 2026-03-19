---
title: 'Bitrefill blames North Korean Lazarus group for cyberattack'
date: 2026-03-19
permalink: /posts/2026/03/19/bitrefill-blames-north-korean-lazarus-group-for-cyberattack/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque de Bitrefill : Implication du groupe Lazarus

La plateforme de commerce électronique Bitrefill a été victime d'une cyberattaque majeure début mars, attribuée au groupe nord-coréen Bluenoroff (sous-groupe de Lazarus/APT38). L'incident a entraîné l'interruption prolongée des services pour sécuriser l'infrastructure. Bien que les soldes des utilisateurs aient été préservés, les attaquants ont accédé à des données transactionnelles concernant 18 500 achats, incluant des adresses e-mail, adresses IP et, pour 1 000 cas, les noms des clients.

**Points clés**
*   **Vecteur d'attaque :** Compromission initiale via l'ordinateur d'un employé, suivie d'une élévation de privilèges.
*   **Méthode :** Utilisation d'identifiants obsolètes pour accéder à des secrets de production, permettant de compromettre l'infrastructure, la base de données et certains portefeuilles « chauds ».
*   **Cible :** Les pirates visaient principalement le vol de cryptomonnaies et de stocks de cartes-cadeaux, plutôt que les données clients.
*   **Impact :** Exposition potentielle de données chiffrées dont les clés de déchiffrement pourraient avoir été compromises.

**Vulnérabilités**
*   **Gestion des accès :** Utilisation d'identifiants hérités (legacy credentials).
*   **Sécurité des secrets :** Stockage ou accès vulnérable à des secrets de production au sein d'instantanés (snapshots) de l'infrastructure.
*   *Note : Aucune CVE spécifique n'est mentionnée dans l'article, l'attaque reposant sur des tactiques, techniques et procédures (TTP) plutôt que sur l'exploitation d'une faille logicielle isolée.*

**Recommandations**
*   **Renforcement des accès :** Mise en œuvre de contrôles d'accès plus stricts et revue des privilèges.
*   **Surveillance accrue :** Amélioration des systèmes de journalisation (logging) et de monitoring pour une détection plus rapide.
*   **Audit de sécurité :** Expansion des revues de sécurité et des tests d'intrusion (pentesting).
*   **Automatisation :** Raffinement des mécanismes d'arrêt automatique des services en cas de détection d'activité suspecte.
*   **Sensibilisation :** Appel à la vigilance des utilisateurs concernant les communications entrantes.

---
[Source](https://www.bleepingcomputer.com/news/security/bitrefill-blames-north-korean-lazarus-group-for-cyberattack/){:target="_blank"}
