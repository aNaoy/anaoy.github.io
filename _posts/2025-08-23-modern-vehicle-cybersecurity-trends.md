---
title: 'Modern vehicle cybersecurity trends'
date: 2025-08-23
permalink: /posts/2025/08/23/modern-vehicle-cybersecurity-trends/
tags:
- veille-cyber
- securelist
---
**La Cybersécurité Automobile : Évolution et Défis Actuels**

Les véhicules modernes, de plus en plus connectés et dotés de systèmes informatiques complexes, offrent de nouvelles fonctionnalités mais élargissent aussi leur surface d'attaque. Si les atteintes à la sécurité fonctionnelle ne sont pas encore généralisées, l'évolution technologique accroît les risques.

Historiquement, les systèmes numériques dans les véhicules ont évolué des unités de contrôle isolées des années 1970 à des réseaux complexes interconnectés via des bus LIN et CAN dans les années 1990. Aujourd'hui, les véhicules intègrent des capacités de communication avancées (5G, V2I, V2V, Wi-Fi, Bluetooth, GPS), avec des points d'entrée potentiels tels que les unités principales (head units) et les modules de télécommunication.

Trois catégories de véhicules sont identifiées :

*   **Véhicules obsolètes :** Peu ou pas d'interaction externe numérique, architecture simple. Les compromissions restent généralement confinées.
*   **Véhicules hérités (Legacy vehicles) :** Présence d'unités télématiques pour la collecte de données et des unités principales plus fonctionnelles. L'architecture est majoritairement numérique, avec des systèmes d'assistance à la conduite, mais les réseaux d'unités de contrôle sont souvent peu segmentés. Ces véhicules représentent un défi majeur, car une compromission peut avoir des conséquences graves sur la sécurité physique. L'exemple du piratage de la Jeep Cherokee est cité.
*   **Véhicules modernes :** Architecture réseau segmentée par des pare-feux via une passerelle centrale, communication bidirectionnelle avec les infrastructures cloud des constructeurs. Les constructeurs ont amélioré la sécurité suite aux découvertes passées, complexifiant les attaques visant la sécurité fonctionnelle.

Malgré ces améliorations, des attaques visant le blocage du démarrage, le verrouillage des portes ou le vol de données restent possibles, souvent via l'infrastructure cloud. Le manque de malwares dédiés et de stratégies de monétisation viables limite actuellement la généralisation des cyberattaques. Cependant, l'adoption de technologies communes (Linux, Android, code open-source) et la disponibilité croissante d'outils d'exploitation des réseaux sans fil pourraient changer la donne.

Les flottes de véhicules (taxis, covoiturage, logistique) et les véhicules spécialisés (poids lourds, transports en commun) sont particulièrement exposés, souvent équipés de systèmes télématiques tiers moins sécurisés et intégrés de manière précaire. Une attaque sur ces flottes peut être très évolutive et causer des pertes financières et réputationnelles considérables.

Pour renforcer la sécurité, des investissements sont nécessaires à tous les niveaux. Les constructeurs multiplient les initiatives : équipes de sécurité produit, gestion des vulnérabilités, tests d'intrusion obligatoires, adoption de méthodologies de développement sécurisé et "security by design". Le déploiement de centres d'opérations de sécurité (SOC) dédiés à l'analyse des données et à la détection d'événements de cybersécurité est également en cours.

**Points Clés :**

*   La connectivité croissante des véhicules accroît la surface d'attaque.
*   Les "legacy vehicles" présentent le risque le plus élevé pour la sécurité fonctionnelle.
*   Les véhicules modernes bénéficient d'une meilleure segmentation réseau.
*   Les flottes et véhicules spécialisés constituent des cibles privilégiées en raison de leur potentiel d'exploitation à grande échelle.
*   L'industrie investit dans la cybersécurité via des équipes dédiées, des tests d'intrusion et des architectures sécurisées.

**Vulnérabilités :**

*   Bien que des CVE spécifiques ne soient pas mentionnées dans cet extrait, les vulnérabilités peuvent exister au niveau des unités principales, des modules de télécommunication, des systèmes d'exploitation (Linux, Android), des composants tiers, des interfaces sans fil (Wi-Fi, Bluetooth, GSM, LTE) et des infrastructures cloud des constructeurs. Les systèmes télématiques tiers intégrés de manière non sécurisée sont également des points faibles identifiés.

**Recommandations :**

*   Investir dans la cybersécurité à tous les niveaux (utilisateur, régulateur, constructeur).
*   Mettre en œuvre des processus de réponse aux rapports de vulnérabilités.
*   Rendre les tests d'intrusion obligatoires dans le cycle de développement.
*   Adopter des méthodologies de développement sécurisé et le "security by design".
*   Exploiter la cybermenace intelligence.
*   Déployer des centres d'opérations de sécurité (SOC) spécialisés pour l'analyse des données des véhicules.

---
[Source](https://securelist.com/automotive-security-trends-2025/117326/){:target="_blank"}
