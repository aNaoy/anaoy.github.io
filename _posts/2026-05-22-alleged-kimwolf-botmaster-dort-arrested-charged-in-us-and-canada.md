---
title: 'Alleged Kimwolf Botmaster ‘Dort’ Arrested, Charged in U.S. and Canada'
date: 2026-05-22
permalink: /posts/2026/05/22/alleged-kimwolf-botmaster-dort-arrested-charged-in-us-and-canada/
tags:
- veille-cyber
- krebs
---
### Arrestation de "Dort", administrateur du botnet Kimwolf

Jacob Butler, un citoyen canadien de 23 ans connu sous le pseudonyme « Dort », a été arrêté à Ottawa suite à une enquête internationale. Il est accusé d'avoir créé et administré **Kimwolf**, un botnet IoT responsable d'attaques par déni de service distribué (DDoS) records, atteignant jusqu'à 30 térabits par seconde.

**Points clés :**
* **Infrastructures ciblées :** Le botnet exploitait des millions d'appareils IoT (caméras, cadres photo numériques) normalement isolés derrière des pare-feux, impactant même des segments réseau du département de la Défense américain.
* **Activités criminelles :** En plus des attaques DDoS (plus de 25 000 commandes d'attaques), le suspect est poursuivi pour harcèlement, doxing et « swatting » contre des chercheurs en cybersécurité ayant exposé ses activités.
* **Opération de démantèlement :** Les autorités américaines et internationales ont saisi en mars 2026 l'infrastructure technique de Kimwolf ainsi que celle de trois autres botnets concurrents (Aisuru, JackSkid et Mossad).
* **Conséquences juridiques :** Butler fait face à des poursuites pénales au Canada et aux États-Unis, avec une demande d'extradition américaine. Il risque jusqu'à 10 ans de prison.

**Vulnérabilités :**
L'article mentionne l'exploitation d'une faille critique non spécifique dans les appareils IoT permettant une propagation rapide du botnet. Bien qu'aucune CVE précise ne soit citée, ces botnets exploitent généralement :
* L'utilisation d'identifiants par défaut sur les appareils IoT.
* Des failles d'exécution de code à distance (RCE) sur des micrologiciels (firmwares) non patchés.
* Des services exposés sur internet via des configurations réseau inadéquates.

**Recommandations :**
* **Sécurisation des terminaux :** Modifier systématiquement les mots de passe par défaut des appareils IoT avant leur connexion au réseau.
* **Segmentation réseau :** Isoler les appareils IoT sur un VLAN distinct, sans accès direct vers ou depuis des segments réseau critiques.
* **Gestion des correctifs :** Appliquer les mises à jour de firmware dès leur publication par les fabricants pour corriger les vulnérabilités exploitées par les botnets.
* **Réduction de la surface d'attaque :** Désactiver les services inutiles (Telnet, UPnP, accès web externe) sur les passerelles et les objets connectés.

---
[Source](https://krebsonsecurity.com/2026/05/alleged-kimwolf-botmaster-dort-arrested-charged-in-u-s-and-canada/){:target="_blank"}
