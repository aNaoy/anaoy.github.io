---
title: 'MLEP in KICS for Networks 5.0: how machine learning helps track network behavior of OT devices'
date: 2026-11-03
permalink: /posts/2026/11/03/mlep-in-kics-for-networks-50-how-machine-learning-helps-track-network-behavior-of-ot-devices/
tags:
- veille-cyber
- securelist
---
### Détection d'anomalies et inventaire dynamique dans les réseaux industriels par le Machine Learning

Dans les environnements industriels, distinguer une activité malveillante d'un échange légitime est complexe, car les attaquants utilisent souvent des outils standards (*Living-off-the-Land*). La détection d'anomalies repose sur une compréhension fine du rôle des équipements et de leurs schémas de communication habituels, des données souvent incomplètes ou obsolètes dans les inventaires classiques.

#### Points clés
*   **Technologie MLEP (Machine Learning Event Processor) :** Intégrée à *Kaspersky Industrial CyberSecurity for Networks*, elle segmente le trafic en flux d'événements de 15 secondes pour analyser les comportements sans stocker chaque paquet, optimisant ainsi les ressources.
*   **Approche neurosémantique (NSN) :** Le système utilise des réseaux neuronaux pour structurer les données en graphes multicouches. Il apprend en temps réel via la "neurogenèse" : si un événement est nouveau, un neurone est créé ; s'il est connu, il est activé.
*   **Inventaire prédictif :** En comparant le comportement réseau des périphériques non identifiés avec ceux déjà répertoriés, le système suggère automatiquement des catégories (ex: PLC, HMI), facilitant la mise à jour des inventaires malgré l'évolution rapide des infrastructures.
*   **Analyse contextuelle :** Le système ne se limite pas aux signatures d'attaques connues mais détecte les déviations statistiques par rapport au profil comportemental spécifique de chaque machine.

#### Types d'anomalies détectées
Le MLEP identifie six scénarios de déviation comportementale :
1.  **Nouveau hôte externe :** Connexion vers une destination inédite.
2.  **Nouvelle combinaison adresse/port :** Utilisation d'un service inhabituel par le périphérique.
3.  **Volume de données atypique :** Transferts de données anormalement élevés.
4.  **Activité en dehors des plages horaires habituelles.**
5.  **Nouveau protocole de communication.**
6.  **Signes de scan :** Tentatives de connexion vers un nombre inhabituel de cibles.

#### Recommandations
*   **Améliorer la visibilité réseau :** Déployer des outils d'inventaire passif et actif pour maximiser la connaissance des actifs, base indispensable à l'efficacité du machine learning.
*   **Exploiter le contexte opérationnel :** Lors d'une alerte, corréler les anomalies détectées par le MLEP avec le rôle métier du dispositif et les autres événements de sécurité pour reconstruire le scénario d'une attaque potentielle.
*   **Maintenance des référentiels :** Utiliser les suggestions de catégorisation du système pour pallier le manque de documentation technique ou le décalage entre les équipements réels et les schémas réseau.

*Note : Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article, celui-ci traitant de la détection comportementale et non de l'exploitation de failles logicielles.*

---
[Source](https://securelist.com/tr/machine-learning-event-processor-in-kics-for-networks/121794/){:target="_blank"}
