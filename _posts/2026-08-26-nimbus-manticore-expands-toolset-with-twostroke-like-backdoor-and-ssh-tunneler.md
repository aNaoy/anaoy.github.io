---
title: 'Nimbus Manticore Expands Toolset With TWOSTROKE-Like Backdoor and SSH Tunneler'
date: 2026-08-26
permalink: /posts/2026/08/26/nimbus-manticore-expands-toolset-with-twostroke-like-backdoor-and-ssh-tunneler/
tags:
- veille-cyber
- hackernews
---
### Expansion des capacités offensives du groupe Nimbus Manticore

Le groupe de cyberespionnage iranien Nimbus Manticore (également connu sous les noms de Tortoiseshell ou UNC1549) intensifie ses activités contre des cibles au Moyen-Orient et en Europe. Affilié au Corps des gardiens de la révolution islamique (IRGC), ce groupe diversifie ses outils pour maintenir un accès persistant sur les réseaux compromis.

**Points clés :**
*   **Stratégie :** Utilisation récurrente d'ingénierie sociale (campagnes « Dream Job ») et déploiement d'infrastructures étendues à travers le Moyen-Orient et l'Europe.
*   **Nouveaux outils :**
    *   Un outil de tunnelisation SSH inversé se faisant passer pour le SDK « Windows Terminal Server ».
    *   Un nouveau cheval de Troie (backdoor) en C++ présentant des similitudes avec le malware **TWOSTROKE**, dissimulé sous le nom de fichier `wtsapi32.dll`.
*   **Fonctionnalités des malwares :** Collecte d'informations système, exécution de fichiers (binaires/DLL), manipulation de fichiers (upload/download), et persistance.
*   **Infrastructure C2 :** Communication via HTTPS sur le port 443 pour les nouveaux implants, avec des serveurs de commande identifiés (ex: `172.86.98[.]113`).

**Vulnérabilités :**
L'article ne mentionne aucune CVE spécifique. Les vecteurs d'attaque reposent principalement sur l'exécution de bibliothèques malveillantes (DLL side-loading) et le recours à des outils légitimes détournés pour établir des tunnels persistants.

**Recommandations :**
*   **Surveillance réseau :** Bloquer et inspecter le trafic sortant vers les adresses IP suspectes (telles que `172.86.98[.]113`) sur le port 443.
*   **Intégrité système :** Vérifier l'intégrité des fichiers système Windows, particulièrement `wtsapi32.dll`, afin de détecter toute substitution par une version malveillante.
*   **Détection d'anomalies :** Surveiller la création de processus inhabituels liés aux services Windows et détecter l'utilisation de tunnels SSH non autorisés dans l'environnement.
*   **Sensibilisation :** Renforcer la vigilance des employés face aux campagnes d'ingénierie sociale basées sur des opportunités d'emploi, vecteur privilégié du groupe.

---
[Source](https://thehackernews.com/2026/08/nimbus-manticore-expands-toolset-with.html){:target="_blank"}
