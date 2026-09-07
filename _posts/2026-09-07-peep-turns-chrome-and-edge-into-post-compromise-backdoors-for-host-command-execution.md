---
title: 'PEEP Turns Chrome and Edge Into Post-Compromise Backdoors for Host Command Execution'
date: 2026-09-07
permalink: /posts/2026/09/07/peep-turns-chrome-and-edge-into-post-compromise-backdoors-for-host-command-execution/
tags:
- veille-cyber
- hackernews
---
### PEEP : Un framework de post-exploitation transformant les navigateurs en backdoors

Le framework **PEEP** est un outil de post-exploitation sophistiqué ciblant les navigateurs basés sur Chromium (Chrome, Edge). Il ne dispose pas de vecteur d'infection initial propre et nécessite une compromission préalable du système hôte par un attaquant. Une fois déployé, il transforme le navigateur en une porte dérobée persistante capable d'exécuter des commandes au niveau du système d'exploitation et de voler des données sensibles.

**Points clés :**
*   **Fonctionnement :** Utilise une extension malveillante (masquée sous le nom "Smart Bookmarks") couplée à un hôte de messagerie native (`nm_host.exe`) pour franchir la sandbox du navigateur et interagir avec l'OS.
*   **Persistance :** Manipule les fichiers de configuration (*Secure Preferences*), utilise le sideloading et exploite les stratégies d'installation forcée (GPO/registre) pour rester actif.
*   **Capacités :** Exfiltration de cookies, historique et données de session ; exécution de commandes shell ; gestion de fichiers ; découverte de processus ; injection de JavaScript.
*   **Origine :** Dérivé du framework open-source *RedExt*. La présence d'artefacts en chinois suggère une origine liée à un acteur russophone ou sinophone.
*   **Infrastructure :** Communique via HTTP en clair avec un serveur de commande et de contrôle (C2), effectuant des battements de cœur (heartbeat) toutes les 30 secondes.

**Vulnérabilités exploitées :**
*   Le malware n'exploite pas une CVE spécifique, mais détourne les fonctionnalités légitimes de **Native Messaging** de Chromium et les mécanismes de gestion des préférences du navigateur.
*   Il abuse des faiblesses de configuration (persistance via *ExtensionInstallForcelist* et modification des fichiers de préférences).

**Recommandations :**
*   **Surveillance des points de terminaison :** Inspecter régulièrement les extensions installées, en particulier celles non issues du Chrome Web Store officiel.
*   **Audit des fichiers :** Surveiller toute modification suspecte des fichiers de préférences de Chrome/Edge (`Secure Preferences`) et la présence de clés de registre liées aux extensions externes (`HKCU\Software\Google\Chrome\Extensions`).
*   **Gestion des privilèges :** Restreindre l'accès administrateur sur les postes de travail, car PEEP nécessite des privilèges élevés pour installer son composant natif (`nm_host.exe`).
*   **Politiques de sécurité :** Auditer les GPO d'entreprise pour s'assurer qu'aucune politique d'installation forcée d'extensions non autorisées n'a été mise en place par un acteur malveillant.
*   **Analyse réseau :** Bloquer ou surveiller les connexions vers les domaines associés (`xfjcc.fun` / `206.237.30.232`) et inspecter les flux HTTP suspects en provenance des processus du navigateur.

---
[Source](https://thehackernews.com/2026/09/peep-turns-chrome-and-edge-into-post.html){:target="_blank"}
