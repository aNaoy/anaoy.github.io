---
title: 'New MODBEACON RAT Uses gRPC Streaming for Encrypted C2 Traffic'
date: 2026-07-10
permalink: /posts/2026/07/10/new-modbeacon-rat-uses-grpc-streaming-for-encrypted-c2-traffic/
tags:
- veille-cyber
- hackernews
---
### Analyse du malware MODBEACON et des activités du groupe Silver Fox

Le groupe cybercriminel **Silver Fox**, lié à la Chine, a déployé un nouveau cheval de Troie d'accès à distance (RAT) nommé **MODBEACON**. Ce malware, développé en Rust, se distingue par une architecture modulaire sophistiquée et l'utilisation de flux gRPC via le framework Xray/V2Ray pour masquer ses communications de commande et contrôle (C2).

**Points clés :**
* **Vecteur d'attaque :** Utilisation intensive du SEO poisoning pour propager des installateurs de logiciels contrefaits via des sites Web frauduleux.
* **Architecture :** Malware résident en mémoire utilisant une séparation entre le chargeur (loader) et le beacon. Il adopte une approche basée sur des plugins pour une exécution flexible.
* **C2 dissimulé :** Le framework C2 tire parti d'outils anti-censure (Xray/V2Ray) pour chiffrer et camoufler ses flux de données, rendant la détection réseau plus complexe.
* **Cibles :** Secteurs de la technologie, de l'éducation et entreprises d'État, principalement en Asie.
* **Profil de l'attaquant :** Silver Fox agit comme un "courtier en trafic" et fournisseur d'accès, combinant des campagnes de fraude à grande échelle avec des intrusions ciblées et persistantes.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée ; l'exploitation repose sur l'ingénierie sociale (téléchargement de logiciels piégés) et l'exécution de code arbitraire par l'utilisateur.

**Fonctionnalités du malware :**
* Identification (fingerprinting) de la machine hôte.
* Chargement et exécution de plugins en mémoire.
* Persistance via des tâches planifiées.
* Exécution de commandes à distance et exfiltration de données.

**Recommandations :**
* **Sensibilisation :** Éduquer les utilisateurs sur les dangers du téléchargement de logiciels à partir de sources non officielles, en particulier suite à des recherches sur les moteurs de recherche (risque de SEO poisoning).
* **Filtrage réseau :** Surveiller les flux suspects utilisant les protocoles de tunnels gRPC ou des communications vers des CDN (Amazon, Cloudflare) non justifiées par l'activité métier.
* **Détection d'endpoint :** Mettre en place des solutions EDR capables de détecter l'exécution de code en mémoire, les injections de plugins et la création de tâches planifiées suspectes.
* **Gestion des privilèges :** Restreindre les droits d'installation des utilisateurs sur les postes de travail pour limiter l'impact des logiciels malveillants exécutés localement.

---
[Source](https://thehackernews.com/2026/07/new-modbeacon-rat-uses-grpc-streaming.html){:target="_blank"}
