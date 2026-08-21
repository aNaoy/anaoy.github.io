---
title: 'The invisible passenger in your car'
date: 2026-08-21
permalink: /posts/2026/08/21/the-invisible-passenger-in-your-car/
tags:
- veille-cyber
- securelist
---
### Infiltration des systèmes automobiles par le groupe MoYu

Des chercheurs ont identifié un nouveau logiciel malveillant Android ciblant spécifiquement les unités centrales (head units) des véhicules. Ce malware, attribué au groupe **MoYu** (lié au botnet BADBOX), utilise une chaîne d'infection sophistiquée pour transformer les systèmes embarqués en outils de fraude publicitaire et en nœuds d'un botnet par procuration.

#### Points clés
*   **Vecteur d'infection :** Le malware est distribué via l'application système légitime `TWCore`, responsable des mises à jour du firmware. Le mécanisme de mise à jour (via le protocole MQTT) permet l'installation forcée d'APK tiers non présents initialement sur le système.
*   **Méthodologie :** Il s'agit d'un malware multi-étapes sans interface utilisateur :
    1.  **JarService (Dropper) :** Décrypte et charge la charge utile suivante.
    2.  **Loader :** Contacte un serveur de commande et contrôle (C2) pour télécharger le module final.
    3.  **Clicker / Reverse Proxy :** Exécute des tâches malveillantes (clics publicitaires, proxy inverse) via des commandes reçues en JSON.
*   **Objectif final :** Utiliser les ressources des véhicules pour créer un botnet de proxys résidentiels, potentiellement monétisé via des services tiers.

#### Vulnérabilités
*   **Abus de fonctionnalité système :** Le détournement de la fonction d'auto-mise à jour `TWCore` (via le flag `installNotExists`) permet l'injection de code malveillant sans interaction de l'utilisateur.
*   **Absence de contrôle d'intégrité :** Le système ne vérifie pas la signature ou la légitimité des paquets téléchargés par l'outil de mise à jour, permettant l'installation de code arbitraire.
*(Note : Aucune CVE spécifique n'est mentionnée, le problème résidant dans la conception même du firmware du vendeur DoFun).*

#### Recommandations
*   **Sécurisation des mises à jour :** Les constructeurs doivent impérativement implémenter une vérification stricte de la signature numérique pour toutes les mises à jour logicielles OTA (Over-The-Air).
*   **Cloisonnement système :** Limiter les privilèges des applications système (`TWCore`) afin qu'elles ne puissent pas installer arbitrairement des applications non signées ou provenant de sources externes non autorisées.
*   **Surveillance réseau :** Surveiller les communications vers les domaines et adresses IP associés (notamment `cardoor[.]cn`, `uipoxy[.]com` et `pxyedge[.]com`) pour détecter toute activité suspecte provenant des unités de bord.
*   **Protection Endpoint :** Déployer des solutions de sécurité capables de détecter les signatures liées au malware (ex: `HEUR:Trojan.AndroidOS.Vo1d.*`).

---
[Source](https://securelist.com/android-head-unit-malware/121106/){:target="_blank"}
