---
title: 'Russian Intelligence Hacks IP Cameras to Spy on Military Logistics Across NATO States and Ukraine'
date: 2026-07-20
permalink: /posts/2026/07/20/russian-intelligence-hacks-ip-cameras-to-spy-on-military-logistics-across-nato-states-and-ukraine/
tags:
- veille-cyber
- hackernews
---
### Espionnage militaire : l'exploitation des caméras IP par le renseignement russe

Des services de renseignement russes exploitent systématiquement des caméras de sécurité connectées à Internet en Europe et en Ukraine pour surveiller les flux logistiques militaires, les mouvements de troupes et le transport d'armements. En Ukraine, ces accès sont détournés pour cibler directement le personnel et les équipements militaires.

**Points clés :**
* **Méthode simple :** Les attaquants n'utilisent pas de "zero-day". Ils scannent le web à la recherche de caméras exposées, utilisant des identifiants par défaut, des firmwares obsolètes ou des configurations d'usine.
* **Automatisation :** Une fois l'accès obtenu, des logiciels de reconnaissance d'image analysent les flux vidéo pour détecter automatiquement des véhicules militaires et des cargaisons.
* **Surface d'exposition :** Plus de 87 000 caméras sont potentiellement exposées dans les zones ciblées. Bien que le nombre de vulnérabilités critiques soit limité, la simple exposition publique des appareils facilite l'intrusion.

**Vulnérabilités mentionnées :**
L'analyse pointe deux vulnérabilités exploitées sur les services embarqués :
* **CVE-2016-7407 :** Vulnérabilité dans l'outil d'importation de clés `dropbearconvert` (serveur SSH Dropbear).
* **CVE-2021-39275 :** Écriture hors limites dans Apache HTTP Server (corrigée dans la version 2.4.49).

**Recommandations :**
* **Isolation réseau :** Désactiver le transfert de port (port-forwarding) et l'UPnP. Accéder aux caméras exclusivement via un VPN.
* **Durcissement :** Remplacer systématiquement les identifiants par défaut par des mots de passe robustes et activer l'authentification multifacteur (MFA).
* **Hygiène logicielle :** Mettre à jour les firmwares et privilégier des équipements bénéficiant d'un support de sécurité sur le long terme.
* **Gestion physique :** Orienter les caméras de manière à masquer les zones sensibles, les quais de chargement et les axes logistiques.
* **Audit :** Identifier les caméras accessibles depuis Internet et vérifier les journaux de connexion pour détecter toute activité suspecte.

---
[Source](https://thehackernews.com/2026/07/russian-intelligence-hacks-ip-cameras.html){:target="_blank"}
