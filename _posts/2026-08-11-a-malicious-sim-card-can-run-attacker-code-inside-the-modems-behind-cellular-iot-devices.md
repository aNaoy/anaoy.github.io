---
title: 'A Malicious SIM Card Can Run Attacker Code Inside the Modems Behind Cellular IoT Devices'
date: 2026-08-11
permalink: /posts/2026/08/11/a-malicious-sim-card-can-run-attacker-code-inside-the-modems-behind-cellular-iot-devices/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité des communications cellulaires : L'attaque par carte SIM malveillante

Des chercheurs ont démontré qu'une carte SIM compromise peut exécuter des commandes arbitraires sur le modem d'un appareil, permettant de prendre le contrôle total d'équipements IoT (bornes de recharge, routeurs industriels, télématique automobile) et de certains smartphones.

**Points clés :**
* **Mécanisme d'attaque :** La faille repose sur la commande « RUN AT », une fonction standard permettant à la carte SIM d'envoyer des commandes AT (langage de contrôle de modem) au processeur de communication.
* **Surface d'attaque :** De nombreux modules IoT intègrent un processeur d'application (souvent sous Linux) qui traite les commandes AT transmises par le modem. Si le filtrage est insuffisant, une injection de commande peut mener à une exécution de code à distance ou à une escalade de privilèges.
* **Risques identifiés :** Downgrade forcé vers la 2G (vulnérable aux stations de base factices), exécution de code, extraction de fichiers sensibles et accès réseau non autorisé.
* **Portée :** 9 appareils sur 26 testés ont été jugés vulnérables, principalement des modules Quectel équipés de processeurs Qualcomm.

**Vulnérabilités :**
* **CVE-2026-57550 :** Interface SIM AT exposée (identifiée également comme CVD-2026-0122 par la GSMA).
* **CVE-2025-48618 :** Faille corrigée dans Android permettant d'ouvrir des pages web via une SIM malveillante.
* **CVE-2021-31698 :** Injection de commande AT précédente sur des daemons similaires.

**Recommandations :**
* **Pour les gestionnaires de flotte IoT :** Contacter les fournisseurs de modules pour vérifier si la commande « RUN AT » est activée dans le firmware et demander sa désactivation si elle n'est pas nécessaire.
* **Pour les fabricants :** Désactiver ou restreindre l'interface « RUN AT » au niveau du firmware. Les nouvelles configurations durcies de Qualcomm visent à désactiver cette interface par défaut.
* **Transparence :** Les constructeurs doivent publier des bulletins de sécurité publics pour permettre aux utilisateurs de vérifier la vulnérabilité de leurs équipements, plutôt que de restreindre l'accès à ces informations derrière des portails privés.

---
[Source](https://thehackernews.com/2026/08/a-malicious-sim-card-can-run-attacker.html){:target="_blank"}
