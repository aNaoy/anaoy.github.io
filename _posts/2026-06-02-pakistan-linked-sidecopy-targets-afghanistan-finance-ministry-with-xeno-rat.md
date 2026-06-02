---
title: 'Pakistan-Linked SideCopy Targets Afghanistan Finance Ministry with Xeno RAT'
date: 2026-06-02
permalink: /posts/2026/06/02/pakistan-linked-sidecopy-targets-afghanistan-finance-ministry-with-xeno-rat/
tags:
- veille-cyber
- hackernews
---
### Opération XENOFISCAL : Le groupe SideCopy cible le ministère des Finances afghan

Le groupe lié au Pakistan, **SideCopy** (affilié à APT36/Transparent Tribe), mène actuellement une campagne d'espionnage baptisée « Opération XENOFISCAL ». Celle-ci vise spécifiquement le ministère des Finances afghan ainsi que divers fonctionnaires provinciaux via des leurres en langue pachto.

#### Points clés
*   **Vecteur d'attaque :** Hameçonnage ciblé (*spear-phishing*) utilisant une archive ZIP contenant un fichier LNK malveillant.
*   **Malware principal :** Xeno RAT (version 1.8.7), un cheval de Troie d'accès à distance complet.
*   **Mécanisme d'infection :** Le fichier LNK exécute `mshta.exe` pour télécharger un fichier HTA distant, lequel déploie un script JavaScript en mémoire. Un chargeur DLL installe ensuite le RAT et un document leurre.
*   **Persistance :** Création d'entrées dans le Registre Windows déguisées en processus Microsoft Edge.
*   **Capacités du RAT :** Enregistrement de frappes clavier, captures d'écran, surveillance webcam/micro, exécution de DLL distantes, tunnel SOCKS5 et vol de données.

#### Vulnérabilités et vecteurs d'exploitation
Bien qu'aucune CVE spécifique ne soit mentionnée, l'attaque repose sur :
*   **Abus de fonctionnalités légitimes :** Utilisation de `mshta.exe` pour contourner les contrôles de sécurité et exécuter du code malveillant.
*   **Ingénierie sociale :** Utilisation de fichiers LNK masqués pour tromper la vigilance des utilisateurs.
*   **Persistance par le Registre :** Manipulation des clés de démarrage automatique de Windows.

#### Recommandations
*   **Sensibilisation :** Former les utilisateurs à la méfiance envers les pièces jointes non sollicitées, même lorsque le nom du fichier est dans la langue locale.
*   **Contrôle des applications :** Restreindre ou surveiller l'exécution des binaires système tels que `mshta.exe`, souvent utilisés pour charger des scripts distants (HTA).
*   **Filtrage réseau :** Bloquer les connexions sortantes vers des domaines ou IP non autorisés, et surveiller le trafic TCP suspect associé aux communications C2 (serveurs de commande).
*   **Politique de sécurité :** Désactiver par défaut l'exécution automatique des fichiers LNK et surveiller les modifications suspectes dans les clés de registre de persistance (Run/RunOnce).

---
[Source](https://thehackernews.com/2026/06/pakistan-linked-sidecopy-targets.html){:target="_blank"}
