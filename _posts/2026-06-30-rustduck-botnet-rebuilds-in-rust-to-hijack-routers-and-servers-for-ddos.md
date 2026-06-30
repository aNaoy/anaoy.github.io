---
title: 'RustDuck Botnet Rebuilds in Rust to Hijack Routers and Servers for DDoS'
date: 2026-06-30
permalink: /posts/2026/06/30/rustduck-botnet-rebuilds-in-rust-to-hijack-routers-and-servers-for-ddos/
tags:
- veille-cyber
- hackernews
---
### RustDuck : Le nouveau botnet DDoS sophistiqué basé sur Rust

RustDuck est un botnet émergent ciblant les routeurs, caméras IP, boîtiers Android et serveurs vulnérables pour orchestrer des attaques par déni de service distribué (DDoS). Bien que de taille modeste, il se distingue par l'utilisation du langage Rust, rendant son analyse complexe, et par des mécanismes avancés d'auto-protection contre la détection.

**Points clés :**
*   **Architecture modulaire :** Fonctionnement en deux étapes (chargeur léger et cœur complexe en Rust).
*   **Persistance et furtivité :** Le malware intègre des vérifications pour détecter s'il s'exécute dans un environnement de recherche (débuggeurs, Wireshark, machines virtuelles, serveurs de test). S'il détecte une analyse, il s'autodétruit.
*   **Communication chiffrée :** Utilisation de protocoles modernes (ChaCha20-Poly1305, AES-GCM, Curve25519) pour masquer ses échanges avec les serveurs de commande (C2).
*   **Infection hybride :** Exploitation massive de mots de passe par défaut (Telnet/SSH) et de vulnérabilités connues sur divers équipements et logiciels.

**Vulnérabilités exploitées :**
*   **CVE-2017-17215 :** RCE sur routeurs Huawei HG532.
*   **CVE-2025-29635 :** Injection de commande sur routeurs D-Link DIR-823X.
*   **CVE-2024-1781 :** Injection de commande sur routeurs Totolink X6000R.
*   **CVE-2018-8007 :** RCE dans Apache CouchDB.
*   *Autres :* Interfaces de débogage Android (ADB) exposées, ainsi que des failles dans ThinkPHP, Jenkins et Hadoop YARN.

**Recommandations :**
*   **Isolation :** Désactiver les accès de gestion à distance (SSH, Telnet, ADB) exposés sur Internet.
*   **Gestion des accès :** Bannir l'usage de mots de passe par défaut sur tous les équipements réseau.
*   **Mises à jour ou remplacement :** Appliquer les correctifs disponibles pour les logiciels serveurs. Pour les routeurs en fin de vie (EOL) ou sans correctifs (comme certains modèles D-Link ou Totolink), le remplacement du matériel est impératif.
*   **Filtrage :** Bloquer les indicateurs de compromission (IoC) connus, notamment les domaines DDNS et les adresses IP sources identifiées par les chercheurs.

---
[Source](https://thehackernews.com/2026/06/rustduck-botnet-rebuilds-in-rust-to.html){:target="_blank"}
