---
title: 'Turn me on, turn me off: Zigbee assessment in industrial environments'
date: 2025-12-12
permalink: /posts/2025/12/12/turn-me-on-turn-me-off-zigbee-assessment-in-industrial-environments/
tags:
- veille-cyber
- securelist
---
## Sécurité des Réseaux Zigbee Industriels : Défis et Attaques

L'article explore les vulnérabilités potentielles des réseaux Zigbee utilisés dans les environnements industriels, en se concentrant sur les spécificités qui les distinguent des déploiements domestiques. Zigbee, un protocole sans fil à faible consommation basé sur IEEE 802.15.4, est privilégié pour sa capacité à gérer un grand nombre de capteurs et sa faible consommation d'énergie, le rendant adapté aux applications où le remplacement des batteries est difficile, voire impossible.

### Points Clés

*   **Protocole Zigbee :** Fonctionne sur la bande de fréquence de 2.4 GHz, partageant cet espace avec d'autres technologies sans fil. Il supporte des réseaux maillés pour étendre la portée et la connectivité.
*   **Types de Périphériques :**
    *   **Coordinateur :** Le cœur du réseau, responsable de son démarrage, de sa gestion et de l'attribution des adresses.
    *   **Routeur :** Amplifie le signal et étend la portée du réseau, permettant la communication entre des nœuds distants.
    *   **Périphérique d'Extrémité (End Device) :** Dispositif le plus économe en énergie, dormant la majeure partie du temps pour préserver la batterie.
*   **Adresses :** Chaque nœud possède une adresse courte (2 octets) et une adresse étendue (8 octets).
*   **Complexité Industrielle :** Les environnements industriels utilisent souvent des profils et des frameworks applicatifs privés, rendant les outils d'analyse standards moins efficaces et nécessitant le développement de solutions personnalisées.

### Vulnérabilités et Vecteurs d'Attaque

L'article détaille deux vecteurs d'attaque principaux :

1.  **Injection de Paquets Spoofés (Spoofed Packet Injection) :**
    *   **Description :** Un attaquant injecte des commandes Zigbee forgées, semblant légitimes, pour déclencher des actions sur un périphérique (par exemple, activer un relais).
    *   **Détails de l'attaque :**
        *   **Capture et Analyse :** Utilisation d'un dongle Nordic Semiconductor nRF52840 avec un firmware "nRF Sniffer" pour capturer le trafic Zigbee. L'analyse se fait via Wireshark.
        *   **Chiffrement :** Le trafic Zigbee est généralement chiffré avec une clé réseau (network key) partagée ou une clé de liaison (link key) spécifique à chaque paire de dispositifs. Même avec le chiffrement, les informations d'en-tête (adresses, PAN ID) restent visibles.
        *   **Déchiffrement :** Nécessite l'obtention de la clé réseau ou de la clé de liaison. Ceci peut être réalisé par :
            *   Utilisation de clés par défaut connues, comme "ZigBeeAlliance09" (problème de sécurité majeur pour les anciennes versions).
            *   Identification du fabricant et recherche de clés par défaut.
            *   Extraction de firmware.
            *   Capture du paquet "transport key" lors d'une réassociation du périphérique.
        *   **Injection :** Nécessite un dongle capable d'émettre des trames brutes (comme le nRF52840 avec Zephyr RTOS). La construction des paquets se fait avec des outils comme Scapy, en imitant la structure des commandes légitimes (APS, ZCL).
        *   **Contre-mesures contre la retransmission :** Les counters de trame Zigbee et potentiellement les counters applicatifs doivent être gérés pour éviter le rejet des paquets.

2.  **Usurpation de Coordinateur (Coordinator Impersonation / Rejoin Attack) :**
    *   **Description :** L'attaquant force un périphérique d'extrémité à quitter son réseau actuel et à rejoindre un coordinateur contrôlé par l'attaquant.
    *   **Détails de l'attaque :**
        *   **Forcer le départ :** Exploitation des conflits de PAN ID (identifiant de réseau) en envoyant des balises (beacons) factices qui poussent le coordinateur légitime à demander à ses appareils de changer de PAN ID et de se réassocier.
        *   **Usurpation :** L'attaquant doit répondre aux requêtes de balises du périphérique d'extrémité avec les mêmes identifiants de réseau (PAN ID, Extended PAN ID) que le coordinateur légitime. L'utilisation d'un champ "Update ID" plus élevé peut parfois inciter le périphérique à choisir le coordinateur usurpateur.
        *   **Défis de synchronisation :** La latence dans la réponse des paquets peut entraîner l'échec de l'association. Une solution consiste à implémenter les fonctions critiques de synchronisation en C sur le firmware du dongle, tandis que la logique de haut niveau est gérée en Python.
        *   **Gestion des clés :** L'obtention de la clé de liaison et le calcul correct de la clé réseau dérivée sont cruciaux pour le succès de l'association. Un outil de calcul de hash de clé de liaison est disponible sur GitHub (klsecservices/zigbee-linkkey-hasher).
        *   **Incompatibilité de Profils :** Les profils de pile propriétaires utilisés dans l'industrie peuvent empêcher les périphériques de rejoindre des réseaux avec des profils publics (comme Zigbee Pro), limitant l'efficacité des firmwares génériques de coordinateur.

### Recommandations

*   **Utiliser les dernières spécifications Zigbee :** Tirer parti des fonctionnalités de sécurité modernes.
*   **Codes d'installation (Installation Codes) :** Utiliser ces codes pour dériver des clés de liaison uniques pour chaque périphérique, plutôt que des clés codées en dur ou par défaut.
*   **Éviter les clés par défaut/codées en dur :** Supprimer ou changer les clés par défaut et s'assurer qu'elles ne sont pas intégrées directement dans les appareils.
*   **Chiffrement de bout en bout :** Compléter le chiffrement au niveau réseau avec un chiffrement de bout en bout au niveau applicatif pour une sécurité accrue, en évitant le modèle de chiffrement uniquement au niveau réseau (hop-by-hop).
*   **Gestion rigoureuse des clés :** Protéger l'accès aux clés réseau et de liaison.
*   **Concevoir des outils personnalisés :** Être préparé à développer des outils et des firmwares spécifiques pour les environnements industriels présentant des profils propriétaires et des complexités uniques.

---
[Source](https://securelist.com/zigbee-protocol-security-assessment/118373/){:target="_blank"}
