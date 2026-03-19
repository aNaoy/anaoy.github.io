---
title: 'Interesting Message Stored in Cowrie Logs, (Wed, Mar 18th)'
date: 2026-03-19
permalink: /posts/2026/03/19/interesting-message-stored-in-cowrie-logs-wed-mar-18th/
tags:
- veille-cyber
- sans-isc
---
### Incursion botnet « iranbot » détectée via les logs Cowrie

Une activité malveillante a été identifiée le 19 février 2026 par des capteurs DShield, révélant une campagne visant les systèmes Linux 64 bits et les objets connectés (IoT). Un acteur malveillant, utilisant l'adresse IP `64.89.161.198`, a réussi des connexions via le protocole Telnet (TCP/23) pour déployer un script d'exploitation. La présence d'une signature spécifique, « MAGIC_PAYLOAD_KILLER_HERE_OR_LEAVE_EMPTY_iranbot_was_here », dans les journaux d'exécution, suggère une signature caractéristique de ce botnet.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation du protocole Telnet (non sécurisé) pour l'accès initial, suivi du téléchargement et de l'exécution d'un script shell malveillant.
*   **Cibles :** Systèmes Linux 64 bits et dispositifs IoT vulnérables.
*   **Trace :** L'attaquant a laissé une trace explicite dans les logs (« iranbot_was_here ») lors de l'exécution d'une commande `echo`.
*   **Période d'activité :** Observée entre fin janvier et fin février 2026, avec un pic d'exploitation le 19 février.

**Vulnérabilités :**
*   **Protocole non sécurisé :** Utilisation persistante de Telnet (TCP/23) pour l'accès aux équipements, ce qui facilite les attaques par force brute ou l'interception. Aucune CVE spécifique n'est mentionnée, l'attaque exploitant directement une mauvaise configuration d'accès distant.

**Recommandations :**
*   **Désactiver Telnet :** Remplacer immédiatement le protocole Telnet par SSH avec une authentification par clé publique et la désactivation de l'accès root à distance.
*   **Durcissement IoT :** Mettre à jour les firmwares des appareils IoT et restreindre leur accès réseau via des pare-feu (isolation VLAN).
*   **Surveillance :** Analyser les logs des serveurs (notamment via des outils comme Cowrie) pour détecter des tentatives d'upload ou d'exécution de scripts suspects.
*   **Filtrage IP :** Bloquer les communications entrantes et sortantes vers les adresses IP suspectes identifiées, telles que `64.89.161.198`.

---
[Source](https://isc.sans.edu/diary/rss/32810){:target="_blank"}
