---
title: 'Unpatched Cacti Zero-Day Enables RCE in Just Four HTTP Requests via Guest Access'
date: 2026-11-27
permalink: /posts/2026/11/27/unpatched-cacti-zero-day-enables-rce-in-just-four-http-requests-via-guest-access/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique de type Zero-Day dans Cacti : exécution de code à distance

Une vulnérabilité de type "zero-day" a été découverte dans la version 1.2.31 de Cacti, l'outil de monitoring réseau open-source. Cette faille permet à un attaquant non authentifié d'obtenir l'exécution de code à distance (RCE) en seulement quatre requêtes HTTP, à condition que le compte « invité » soit activé.

**Points clés :**
*   **Vecteur d'attaque :** L'attaque exploite l'accès invité pour injecter une chaîne de caractères non valide dans le paramètre de configuration `preview_graphs_per_page`.
*   **Chaînage d'exploitation :** L'absence de validation des entrées permet une injection SQL de second ordre, modifiant la table `poller`. Le système exécute ensuite ces données via la fonction PHP `popen()` sans aucun filtrage, menant à une exécution de code arbitraire.
*   **Impact :** Compromission totale du serveur Cacti. Étant donné que ces serveurs centralisent souvent les identifiants et les accès réseau, cette faille constitue un point d'entrée critique pour un mouvement latéral sur l'ensemble du réseau.

**Vulnérabilité :**
*   **CVE :** Non assignée (suivie sous les noms « 4HTTP2SHELL » ou « 4HTTP2ROOT »).

**Recommandations :**
*   **Désactivation immédiate :** Désactiver le compte invité sur toutes les instances Cacti (il est désactivé par défaut depuis la version 0.8.7, mais peut être réactivé manuellement).
*   **Restriction d'accès :** Restreindre l'accès à l'interface web de Cacti aux seules adresses IP de confiance via des listes de contrôle d'accès (ACL) ou un VPN.
*   **Audit de sécurité :** Vérifier les entrées de configuration du "poller" pour détecter toute commande suspecte ou modification inhabituelle des paramètres.
*   **Veille :** Surveiller les communications officielles de Cacti pour l'application du correctif dès sa publication.

---
[Source](https://thehackernews.com/2026/11/unpatched-cacti-zero-day-enables-rce-in.html){:target="_blank"}
