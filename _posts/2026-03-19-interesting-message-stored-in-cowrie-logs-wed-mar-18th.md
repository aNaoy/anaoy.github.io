---
title: 'Interesting Message Stored in Cowrie Logs, (Wed, Mar 18th)'
date: 2026-03-19
permalink: /posts/2026/03/19/interesting-message-stored-in-cowrie-logs-wed-mar-18th/
tags:
- veille-cyber
- sans-isc
---
### Analyse d'une campagne de compromission par botnet "iranbot"

Des sondes DShield ont détecté une activité malveillante significative le 19 février 2026, impliquant des tentatives d'exploitation de systèmes Linux 64 bits et d'appareils IoT. Les attaquants ont utilisé l'adresse IP `64.89.161.198` pour effectuer des scans de ports et des connexions Telnet (TCP/23) réussies.

**Points clés :**
* **Signature de l'attaque :** Les logs du honeypot Cowrie ont révélé l'exécution d'une commande contenant la chaîne `MAGIC_PAYLOAD_KILLER_HERE_OR_LEAVE_EMPTY_iranbot_was_here`.
* **Mode opératoire :** Le botnet déploie des scripts shell après authentification via Telnet pour infecter les cibles.
* **Ciblage :** La campagne vise spécifiquement les systèmes Linux 64 bits et les équipements IoT vulnérables aux accès Telnet non sécurisés.

**Vulnérabilités :**
* Utilisation du protocole Telnet (TCP/23) pour l'accès à distance, protocole non chiffré et notoirement vulnérable aux attaques par force brute.
* Absence de CVE spécifique mentionnée, mais exploitation générique de services distants faiblement sécurisés sur des systèmes IoT et Linux.

**Recommandations :**
* **Désactivation de Telnet :** Remplacer systématiquement Telnet par SSH avec authentification par clé publique et désactivation de l'accès root à distance.
* **Durcissement des équipements IoT :** Modifier les identifiants par défaut des appareils et limiter l'exposition de leurs interfaces de gestion sur Internet.
* **Surveillance réseau :** Bloquer le trafic provenant de l'IP malveillante identifiée (`64.89.161.198`) et surveiller les logs pour détecter des tentatives de connexion suspectes sur le port 23.
* **Analyse de fichiers :** Utiliser des outils comme VirusTotal pour vérifier l'intégrité des scripts ou binaires suspects trouvés sur les serveurs (Hachage SHA-256 du script identifié : `f1c0e109640d154246d27ff05074365740e994f142ef9846634bec7b18e3b715`).

---
[Source](https://isc.sans.edu/diary/rss/32810){:target="_blank"}
