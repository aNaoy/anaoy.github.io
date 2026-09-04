---
title: 'Angry Birds: Toy Ghouls’ new toys'
date: 2026-09-04
permalink: /posts/2026/09/04/angry-birds-toy-ghouls-new-toys/
tags:
- veille-cyber
- securelist
---
### Montée en sophistication du groupe Toy Ghouls : Analyse des nouveaux backdoors « Bird »

Le groupe cybercriminel Toy Ghouls (également connu sous les noms de Bearlyfy, Laboo.boo ou Feral Wolf) a fait évoluer ses méthodes en abandonnant l'usage exclusif d'outils publics au profit de backdoors propriétaires. Ces outils, baptisés `mqtt-bird-agent` et `matrix-bird-agent`, permettent une prise de contrôle totale des systèmes infectés en détournant des infrastructures légitimes pour leurs communications.

**Points clés :**
* **Vecteur d'infection :** Utilisation de WinRM (via *Evil-WinRM* ou *WinRM-fs*) pour le déploiement.
* **Persistance :** Installation en tant que services Windows (ex: `cplsupport`, `wtas`).
* **Canaux de communication C2 non conventionnels :**
    * **HiveMQ :** Utilisation du broker MQTT public pour échanger des commandes et exfiltrer des métriques.
    * **Element (Matrix) :** Utilisation d'un serveur Element privé où un bot (`panel-bot`) envoie des commandes via des messages dans des salons dédiés.
* **Mécanismes de protection :** Chiffrement des fichiers de configuration via ChaCha20-Poly1305, lié à l'identifiant matériel (`MachineGuid`) de la machine infectée.

**Vulnérabilités exploitées :**
* Aucune CVE spécifique n'est mentionnée ; le groupe exploite principalement des vecteurs d'administration légitimes (WinRM) et des services tiers détournés (HiveMQ, Matrix).

**Recommandations :**
* **Surveillance réseau :** Bloquer ou surveiller les connexions sortantes vers des services de messagerie ou des brokers MQTT suspects non autorisés dans l'environnement professionnel.
* **Durcissement WinRM :** Restreindre strictement l'accès à WinRM et surveiller l'exécution de scripts PowerShell distants non justifiés.
* **Intégrité du registre :** Surveiller les accès et modifications sur les clés liées aux agents identifiés (`HKLM\Software\synapse\...` et `HKLM\Software\SynapseAgent\...`).
* **Détection :** Utiliser les indicateurs de compromission (IoC) fournis (hashes MD5 de `cplsupport.exe` et `wtass.exe`) pour scanner le parc informatique et identifier les processus malveillants associés.

---
[Source](https://securelist.com/toy-ghouls-new-hivemq-and-element-backdoors/121270/){:target="_blank"}
