---
title: 'Network Anomaly Detection in KATA'
date: 2026-07-31
permalink: /posts/2026/07/31/network-anomaly-detection-in-kata/
tags:
- veille-cyber
- securelist
---
### Détection des menaces par analyse d'anomalies réseau (NAD) avec KATA

Les outils de sécurité traditionnels basés sur les signatures sont inefficaces face aux attaques utilisant des protocoles légitimes de l'infrastructure réseau (Kerberos, DNS). La plateforme **Kaspersky Anti Targeted Attack (KATA)** utilise l'analyse d'anomalies réseau (NAD) pour identifier ces comportements malveillants en s'appuyant sur des modèles comportementaux plutôt que sur des signatures statiques.

#### Points clés
*   **Approche comportementale :** Le NAD analyse les écarts par rapport au profil d'activité normal d'un hôte ou d'un utilisateur.
*   **Réduction du bruit :** En corrélant des indicateurs indirects et en utilisant des seuils personnalisables, le système limite les faux positifs que généreraient des outils basés uniquement sur les signatures.
*   **Flexibilité :** KATA utilise des requêtes SQL sur une base de données ClickHouse, permettant aux analystes d'ajuster les règles de détection via des variables (ex: exclusions d'hôtes, seuils de volume).

#### Détection du Kerberoasting
L'attaque exploite le protocole Kerberos pour demander des tickets (TGS-REQ) afin de craquer hors ligne les mots de passe des comptes de service.
*   **Anomalie détectée :** Un hôte reçoit un nombre inhabituel de tickets (TGS-REP) pour des services uniques (SPN) dans un court laps de temps.
*   **Logique NAD :** Agrégation des réponses TGS-REP par hôte source et par utilisateur, en excluant les services systèmes connus et les comptes légitimes.

#### Détection du tunneling DNS
Les attaquants utilisent des requêtes DNS (notamment via des enregistrements TXT) pour exfiltrer des données ou établir une communication C2.
*   **Anomalie détectée :** Utilisation répétée de sous-domaines longs et variables associés à un domaine racine statique, couplée à un volume de données anormalement élevé dans les réponses DNS.
*   **Logique NAD :** Surveillance du volume de données (champs `rrname` + `rdata`) par hôte source, en excluant les serveurs DNS internes légitimes.

#### Recommandations
*   **Personnalisation des règles :** Ne pas utiliser les règles "telles quelles" ; définir précisément les serveurs DNS de l'infrastructure, les sous-réseaux critiques et les comptes de service exclus dans les variables des règles NAD.
*   **Analyse contextuelle :** Lors du déclenchement d'une alerte, examiner les sessions réseau associées pour visualiser l'ensemble des échanges et confirmer la malignité.
*   **Maintenance :** Tirer parti des 59 modèles préconfigurés dans KATA et les adapter régulièrement pour suivre l'évolution de l'infrastructure réseau.

---
[Source](https://securelist.com/tr/network-anomaly-detection-in-kata/120892/){:target="_blank"}
