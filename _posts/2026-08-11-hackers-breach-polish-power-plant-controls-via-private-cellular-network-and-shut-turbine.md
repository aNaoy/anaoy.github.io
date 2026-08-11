---
title: 'Hackers Breach Polish Power Plant Controls via Private Cellular Network and Shut Turbine'
date: 2026-08-11
permalink: /posts/2026/08/11/hackers-breach-polish-power-plant-controls-via-private-cellular-network-and-shut-turbine/
tags:
- veille-cyber
- hackernews
---
### Sabotage d'une centrale électrique polonaise via une faille réseau privée

En décembre 2025, une centrale thermique polonaise a subi une attaque paralysant sa turbine et son système de traitement d'eau. Les attaquants ont exploité une configuration permissive d'un réseau cellulaire privé (APN) pour pivoter d'un réseau compromis (ferme éolienne) vers les contrôleurs industriels (OT) de la centrale.

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'un APN privé mal segmenté permettant une communication inter-appareils (client-to-client).
* **Progression :** L'attaquant a compromis un pare-feu FortiGate (VPN sans MFA), puis utilisé un routeur Teltonika RUTX50 comme point d'entrée dans le réseau OT.
* **Méthode :** Aucune malveillance logicielle n'a été utilisée. Les attaquants ont exploité les fonctions légitimes des équipements (SSH, interfaces web) pour arrêter les automates programmables (API Siemens) et réinitialiser les équipements réseau.
* **Dissimulation :** Les attaquants ont effacé leurs traces en corrompant la table de partition du contrôleur WAGO et en réinitialisant les routeurs/pare-feux aux paramètres d'usine.

**Vulnérabilités identifiées :**
* **Absence d'isolation :** Les appareils sur l'APN privé pouvaient communiquer librement entre eux.
* **Credentials par défaut :** Le contrôleur WAGO PFC200 était accessible via son interface web avec ses identifiants d'origine.
* **Faiblesses de configuration :** VPN exposé sans authentification multi-facteurs (MFA) et services de gestion inutiles exposés sur les interfaces réseau.
* **CVE mentionnées dans le rapport (contexte) :** Bien que non exploitées directement, le rapport cite CVE-2023-32349 et CVE-2023-32350 concernant les routeurs Teltonika comme risques potentiels de privilèges.

**Recommandations :**
* **Segmentation réseau :** Activer l'isolation des clients au sein des APN privés et traiter les réseaux cellulaires comme des zones non fiables (Untrusted).
* **Sécurisation des accès :** Appliquer une authentification multi-facteurs (MFA) systématique sur tous les accès distants et remplacer impérativement tous les mots de passe par défaut.
* **Durcissement OT :** Désactiver les services de gestion non nécessaires sur les interfaces accessibles, restreindre le trafic entrant et mettre en place une segmentation rigoureuse entre les sites (éolien vs centrale thermique).
* **Audit :** Vérifier régulièrement les configurations des APN pour s'assurer qu'aucune communication latérale non autorisée n'est possible.

---
[Source](https://thehackernews.com/2026/08/hackers-breach-polish-power-plant.html){:target="_blank"}
