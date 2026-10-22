---
title: 'How APT41 revived the BlackLotus bootkit to attack diplomatic organizations in Central Asia'
date: 2026-10-22
permalink: /posts/2026/10/22/how-apt41-revived-the-blacklotus-bootkit-to-attack-diplomatic-organizations-in-central-asia/
tags:
- veille-cyber
- securelist
---
### Résurgence du bootkit BlackX par le groupe APT41

Le groupe APT41 a récemment déployé le bootkit « BlackX » pour cibler des organisations diplomatiques en Asie centrale. Ce malware est une variante perfectionnée du célèbre bootkit BlackLotus, capable de contourner le protocole *Secure Boot* pour injecter des pilotes malveillants au niveau du noyau Windows, permettant ainsi une surveillance persistante.

**Points clés :**
* **Attribution :** APT41 (liens probables avec le groupe FishMonger et usage d'outils d'obfuscation OLLVM).
* **Mode opératoire :** Installation post-compromission via un exécutable légitime détourné (*DLL sideloading*), dissimulant des composants chiffrés.
* **Persistance :** Utilisation du stockage cloud (Google Drive, OneDrive, Yandex.Disk) pour le contrôle et la commande (C2) et déploiement de charges utiles en Rust.
* **Vulnérabilité exploitée :** Baton Drop (**CVE-2022-21894**).

**Vulnérabilité et défaillance de sécurité :**
Bien que les machines cibles soient à jour, elles restaient vulnérables. La faille réside dans le processus de remédiation de Microsoft : le correctif pour la CVE-2022-21894 nécessite une activation manuelle complexe (modification du registre et planification de tâche) pour révoquer le certificat compromis. De nombreux administrateurs ignorent cette étape, laissant les systèmes exposés malgré l'installation du correctif.

**Recommandations :**
* **Validation des correctifs :** Ne pas se contenter de l'installation des mises à jour ; vérifier les notes techniques de l'éditeur pour confirmer si une configuration post-installation (activation manuelle de révocation de certificat) est nécessaire.
* **Sécurité multicouche :** Déployer des solutions de sécurité équipées de modules de prévention des exploits (Exploit Prevention) capables d'intercepter les attaques au niveau du noyau, même si le correctif n'est pas pleinement appliqué.
* **Surveillance :** Surveiller les alertes de sécurité liées aux comportements anormaux des pilotes et aux tentatives de désactivation des solutions de protection (ETW, callbacks de processus).

---
[Source](https://securelist.com/uefi-bootkit-blackx/121539/){:target="_blank"}
