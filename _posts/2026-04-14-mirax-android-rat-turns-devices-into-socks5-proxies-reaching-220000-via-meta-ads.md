---
title: 'Mirax Android RAT Turns Devices into SOCKS5 Proxies, Reaching 220,000 via Meta Ads'
date: 2026-04-14
permalink: /posts/2026/04/14/mirax-android-rat-turns-devices-into-socks5-proxies-reaching-220000-via-meta-ads/
tags:
- veille-cyber
- hackernews
---
### Menace Mirax : Transformer les appareils Android en nœuds proxy malveillants

Le cheval de Troie d'accès à distance (RAT) **Mirax** cible activement les utilisateurs Android, particulièrement dans les pays hispanophones. Ce malware se distingue par sa capacité à transformer les appareils infectés en nœuds de proxy résidentiels via le protocole SOCKS5, permettant aux attaquants de détourner l'adresse IP des victimes pour mener des fraudes ou contourner des restrictions géographiques.

**Points clés :**
* **Vecteur de distribution :** Publicités Meta (Facebook, Instagram) promettant l'accès gratuit à du contenu en streaming, redirigeant vers des sites de téléchargement d'applications "droppers" hébergées sur GitHub.
* **Modèle économique :** Vendu sous forme de Malware-as-a-Service (MaaS) sur des forums underground pour environ 2 500 $ (trimestriel).
* **Technique d'infection :** Utilisation de "crypters" (Virbox, Golden Crypt) pour contourner la détection, nécessitant l'activation des services d'accessibilité pour dissimuler ses activités sous une fausse interface.
* **Portée :** Plus de 220 000 comptes touchés, avec une sélection stricte des affiliés (priorité aux acteurs russophones).

**Vulnérabilités exploitées :**
* Aucune CVE spécifique n'est mentionnée ; l'exploitation repose sur l'**ingénierie sociale** et le contournement des sécurités Android par l'incitation à l'installation de sources inconnues et l'octroi de droits d'accessibilité abusifs.

**Recommandations de sécurité :**
* **Éviter les sources non officielles :** Ne jamais télécharger d'applications en dehors du Google Play Store, en particulier celles promues via des publicités sur les réseaux sociaux.
* **Gérer les permissions :** Être extrêmement vigilant concernant les demandes d'activation des "services d'accessibilité" pour des applications tierces, car ces droits sont souvent détournés par les RAT pour prendre le contrôle total de l'appareil.
* **Sécurité des paramètres :** Désactiver l'option "Installer des applications de sources inconnues" dans les paramètres de sécurité Android.
* **Vigilance publicitaire :** Se méfier des offres trop alléchantes (streaming gratuit, contenu premium) diffusées via des publicités sponsorisées sur les plateformes sociales.

---
[Source](https://thehackernews.com/2026/04/mirax-android-rat-turns-devices-into.html){:target="_blank"}
