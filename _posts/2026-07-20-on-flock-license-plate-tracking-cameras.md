---
title: 'On Flock License Plate Tracking Cameras'
date: 2026-07-20
permalink: /posts/2026/07/20/on-flock-license-plate-tracking-cameras/
tags:
- veille-cyber
- schneier
---
### Défaillances et dérives du système de surveillance par plaques d'immatriculation Flock

Le réseau de caméras de surveillance Flock Safety est au cœur d'une controverse après qu'un journaliste a été arrêté à tort en raison d'une erreur de correspondance de plaque d'immatriculation. Le système, conçu pour alerter les autorités, génère des faux positifs massifs en raison de sa configuration algorithmique, tout en soulevant des inquiétudes croissantes sur l'usage détourné de cette technologie.

**Points clés**
*   **Erreur algorithmique :** Le système de reconnaissance optique (ML) est configuré pour déclencher une alerte dès qu'une partie des caractères recherchés est détectée, entraînant des correspondances erronées sur des véhicules dont la plaque ne correspond que partiellement au signalement.
*   **Surveillance étendue :** Au-delà des plaques d'immatriculation, les forces de l'ordre utilisent le réseau pour traquer des individus sur la base de critères physiques (vêtements, accessoires, corpulence) ou de leur affiliation politique, transformant le système en outil de surveillance de masse des personnes.
*   **Responsabilité diluée :** Flock rejette la responsabilité des erreurs sur les utilisateurs (la police), affirmant que le système fonctionne comme demandé, tandis que les autorités peinent à corriger les données erronées insérées dans le réseau, créant un effet domino à l'échelle nationale.
*   **Comportement corporatif :** Le PDG de l'entreprise a dû présenter des excuses publiques après avoir qualifié les militants pour la protection de la vie privée de « terroristes », illustrant une stratégie de communication agressive face aux critiques.

**Vulnérabilités identifiées**
*   **Absence de contrôle de précision (Validation de match) :** Le logiciel manque de garde-fous pour exiger une correspondance exacte, privilégiant une sensibilité maximale qui favorise les faux positifs.
*   **Intégrité des données :** Le processus de saisie manuelle par les forces de l'ordre est sujet aux erreurs (troncature de plaques), lesquelles se propagent immédiatement dans tout le réseau automatisé sans vérification humaine préalable.
*   **Dérive de finalité (Function Creep) :** Le passage d'un outil de lecture de plaques à un système de reconnaissance faciale et morphologique automatisé s'opère sans cadre éthique ou technique rigoureux, exposant les citoyens à des dérives de profilage.

**Recommandations**
*   **Imposer une correspondance stricte :** Configurer les algorithmes pour exiger une correspondance complète de la plaque d'immatriculation avant l'émission d'une alerte, afin d'éliminer les faux positifs basés sur des correspondances partielles.
*   **Standardisation de l'audit :** Mettre en place des audits externes indépendants et réguliers sur les requêtes effectuées dans la base de données pour prévenir les abus policiers et le profilage ciblé.
*   **Mécanismes de correction en temps réel :** Développer un protocole d'urgence pour la mise à jour des données au sein du réseau, afin de limiter la propagation d'erreurs d'identification lors d'enquêtes en cours.
*   **Transparence algorithmique :** Soumettre le fonctionnement du système de surveillance à une supervision publique stricte pour limiter la collecte de données nominatives ne concernant pas directement des véhicules suspects.

---
[Source](https://www.schneier.com/blog/archives/2026/07/on-flock-license-plate-tracking-cameras.html){:target="_blank"}
