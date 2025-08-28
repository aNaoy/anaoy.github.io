---
title: 'Shadow IT Is Expanding Your Attack Surface. Here’s Proof'
date: 2025-08-28
permalink: /posts/2025/08/28/shadow-it-is-expanding-your-attack-surface-heres-proof/
tags:
- veille-cyber
- bleepingcomp
---
Voici un résumé concis de l'article :

**Les Risques Cachés du Shadow IT : Une Évaluation Réelle**

L'utilisation de systèmes et d'applications non autorisés par les équipes de sécurité informatiques, connue sous le nom de "Shadow IT", représente un défi persistant pour la cybersécurité. Ces actifs non gérés constituent des points d'entrée potentiels pour les attaquants.

Une analyse rapide a permis de découvrir plusieurs exemples concrets de ces expositions, notamment :

*   **Sauvegardes non sécurisées :** Des archives de sauvegarde facilement téléchargeables, contenant des identifiants actifs, du code source d'applications et des dumps de bases de données.
*   **Répertoires Git publics avec des secrets :** Des dépôts de code ouverts qui conservent dans leur historique des informations sensibles (clés API, identifiants de bases de données) qui sont toujours valides.
*   **Panneaux d'administration sans authentification :** Des interfaces d'administration pour des systèmes de journalisation ou de surveillance (comme Elasticsearch) exposées publiquement sans aucune protection, certaines montrant des signes d'activité malveillante passée.
*   **Mauvaises configurations généralisées :** Une seule mauvaise configuration répétée sur une centaine de domaines, exposant des fichiers de sauvegarde d'applications et de bases de données.

Ces vulnérabilités, souvent dues à une mauvaise gestion ou à une faible hygiène des développeurs, n'ont nécessité aucune technique d'exploitation avancée pour être exploitées et contenaient des données très sensibles.

**Points Clés :**

*   Le Shadow IT crée des "angles morts" dans la posture de sécurité d'une organisation.
*   La découverte continue des sous-domaines est une méthode efficace pour identifier les systèmes cachés.
*   Les données sensibles, les identifiants et le code source sont fréquemment exposés dans des actifs Shadow IT.
*   Les vulnérabilités découvertes étaient faciles à exploiter et les données compromises représentaient un risque significatif.

**Vulnérabilités et Recommandations :**

Les vulnérabilités typiquement trouvées dans les contextes de Shadow IT incluent :

*   **Exposition de répertoires de sauvegarde (sans CVE spécifique, mais la pratique est commune)** : Permet le téléchargement non autorisé de données sensibles.
*   **Secrets persistants dans l'historique Git (sans CVE spécifique)** : Utilisation d'identifiants et de clés d'API exposés via le contrôle de version.
*   **Accès non authentifié aux panneaux d'administration (sans CVE spécifique)** : Accès ouvert à des interfaces critiques comme Elasticsearch.
*   **Mauvaises configurations de fichiers (sans CVE spécifique)** : Diffusion de code source ou de sauvegardes de bases de données par défaut.

**Recommandations :**

*   **Énumération continue des sous-domaines :** Pour découvrir de nouveaux systèmes avant les attaquants.
*   **Intégration des actifs découverts dans le programme de gestion des vulnérabilités :** Pour s'assurer qu'aucun système n'est oublié.
*   **Utilisation de solutions de gestion de la surface d'attaque :** Pour automatiser la découverte d'actifs inconnus et leur scan pour les vulnérabilités.

---
[Source](https://www.bleepingcomputer.com/news/security/shadow-it-is-expanding-your-attack-surface-heres-proof/){:target="_blank"}
