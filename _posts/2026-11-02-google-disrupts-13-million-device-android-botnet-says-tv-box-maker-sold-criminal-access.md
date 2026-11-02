---
title: 'Google Disrupts 1.3 Million-Device Android Botnet, Says TV Box Maker Sold Criminal Access'
date: 2026-11-02
permalink: /posts/2026/11/02/google-disrupts-13-million-device-android-botnet-says-tv-box-maker-sold-criminal-access/
tags:
- veille-cyber
- hackernews
---
### Démantèlement du botnet Android : La complicité d'un fabricant mise en cause

Google a récemment dirigé une opération internationale visant à neutraliser un botnet massif de plus de 1,3 million d'appareils Android, principalement des boîtiers TV (Android TV). L'enquête révèle que le fabricant chinois **Videostrong** aurait délibérément intégré une porte dérobée (*backdoor*) nommée **x.cpe** dans ses firmwares pour faciliter des activités criminelles.

**Points clés :**
*   **Nature de la menace :** Le botnet était utilisé pour la fraude publicitaire et la vente de bande passante domestique via des services de proxys résidentiels, permettant à des tiers de faire transiter du trafic illicite via les connexions privées des utilisateurs.
*   **Fonctionnement de la porte dérobée :** Présente au niveau du système (firmware), la porte dérobée permettait aux attaquants d'installer des logiciels à l'insu des utilisateurs, de capturer des écrans, d'intercepter des saisies clavier et d'exécuter des commandes à distance.
*   **Portée :** Plus de 1,47 million d'appareils infectés identifiés à travers 206 modèles différents (incluant des boîtiers TV, mais aussi du matériel de télésanté et de signalétique numérique).
*   **Sanctions :** Google a banni Videostrong et ses filiales de l'écosystème Android certifié.

**Vulnérabilités :**
*   **x.cpe (Backdoor système) :** Ce malware, intégré directement dans le firmware, contourne la sécurité intégrée (Google Play Protect) en désactivant ses vérifications d'applications. Il ne possède pas de CVE spécifique, car il s'agit d'une compromission intentionnelle de la chaîne d'approvisionnement (*Supply Chain Attack*).

**Recommandations :**
*   **Pour les particuliers :** Étant donné que la porte dérobée réside dans le firmware et se réinstalle après un redémarrage, la suppression totale est quasi impossible par l'utilisateur. La recommandation forte des experts est de **cesser l'utilisation de ces appareils** et de les remplacer.
*   **Pour les entreprises :**
    *   Identifier et isoler les appareils MECOOL ou tout matériel suspect sur le réseau professionnel.
    *   Bloquer les domaines et adresses IP liés aux serveurs de commande (C2) identifiés par les rapports de sécurité (ex: Synthient, Plume).
    *   Segmenter le réseau pour séparer strictement les objets connectés grand public des systèmes informatiques critiques.
    *   Considérer tous les appareils domestiques non gérés comme des vecteurs d'attaque potentiels pour le personnel en télétravail.

---
[Source](https://thehackernews.com/2026/11/google-disrupts-13-million-device.html){:target="_blank"}
