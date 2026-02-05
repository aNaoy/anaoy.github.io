---
title: 'Hackers compromise NGINX servers to redirect user traffic'
date: 2026-02-05
permalink: /posts/2026/02/05/hackers-compromise-nginx-servers-to-redirect-user-traffic/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de serveurs NGINX pour le détournement de trafic

Une campagne malveillante détourne le trafic des utilisateurs en modifiant les configurations de serveurs NGINX, les redirigeant vers une infrastructure contrôlée par les attaquants. Cette menace cible particulièrement les installations NGINX utilisées avec les panneaux de gestion d'hébergement Baota, notamment sur les sites ayant des domaines de premier niveau asiatiques (.in, .id, .pe, .bd, .th) ainsi que des sites gouvernementaux et éducatifs (.edu, .gov).

Les attaquants injectent des blocs de configuration NGINX malveillants qui interceptent les requêtes entrantes sur des chemins d'URL spécifiques. Ces requêtes sont ensuite modifiées pour inclure l'URL d'origine complète et transmises via la directive `proxy_pass` à des domaines sous le contrôle des cybercriminels. Les en-têtes de requêtes légitimes sont préservés pour masquer l'activité frauduleuse.

L'attaque repose sur un kit d'outils scripté en cinq étapes :
1.  **zx.sh** : Orchestre le téléchargement et l'exécution des autres étapes.
2.  **bt.sh** : Modifie les configurations NGINX gérées par le panel Baota.
3.  **4zdh.sh** : Cherche les emplacements de configuration NGINX courants, valide les modifications et recharge NGINX.
4.  **zdh.sh** : Ciblage plus précis, notamment pour les domaines .in et .id, avec un processus similaire de validation et de rechargement.
5.  **ok.sh** : Rassemble les informations sur les domaines détournés et les cibles de proxy pour les exfiltrer vers un serveur de commande et contrôle.

La discrétion de cette menace réside dans le fait qu'elle n'exploite pas de vulnérabilité logicielle directe mais dissimule des instructions malveillantes dans les fichiers de configuration, rarement audités. De plus, le trafic atteint sa destination finale, rendant le passage par l'infrastructure de l'attaquant difficile à détecter sans surveillance spécifique.

**Points Clés :**
*   Détournement de trafic utilisateur via la modification de configurations NGINX.
*   Ciblage des panneaux d'hébergement Baota sur des domaines asiatiques, gouvernementaux et éducatifs.
*   Utilisation de la directive `proxy_pass` pour rediriger le trafic de manière transparente.
*   Mécanisme d'attaque en cinq étapes pour automatiser la compromission et l'exfiltration.
*   Difficulté de détection due à l'absence d'exploitation de vulnérabilité directe et à la préservation de l'apparence légitime du trafic.

**Vulnérabilités :**
*   Aucune vulnérabilité logicielle NGINX spécifique n'est mentionnée dans l'article. L'attaque exploite l'accès et la modification des fichiers de configuration.

**Recommandations :**
*   Surveiller attentivement les fichiers de configuration NGINX pour toute modification suspecte ou injection de blocs malveillants.
*   Auditer régulièrement les configurations NGINX, particulièrement celles gérées par des panels d'hébergement.
*   Mettre en place une surveillance réseau poussée pour détecter les flux de trafic anormaux ou les redirections inattendues.
*   Sécuriser l'accès aux panneaux de gestion d'hébergement et aux configurations serveur.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-compromise-nginx-servers-to-redirect-user-traffic/){:target="_blank"}
