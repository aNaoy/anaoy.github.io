---
title: 'Unpatched XRING Flaw in XQUIC Lets Remote Clients Crash HTTP/3 Servers'
date: 2026-07-10
permalink: /posts/2026/07/10/unpatched-xring-flaw-in-xquic-lets-remote-clients-crash-http3-servers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité XRING : Crash critique dans la bibliothèque XQUIC

Une faille de sécurité, baptisée **XRING**, affecte la bibliothèque open-source XQUIC d'Alibaba (utilisée notamment dans le serveur Tengine). Elle permet à n'importe quel client distant de provoquer un déni de service (crash du serveur) en envoyant une séquence de trafic HTTP/3 parfaitement légitime.

**Points clés :**
* **Origine du problème :** Une erreur de calcul arithmétique dans la gestion de la compression d'en-têtes QPACK. Lors du redimensionnement du tampon circulaire (*ring buffer*) utilisé pour les tables de compression, le système calcule mal la taille des données à déplacer.
* **Conséquence :** Une soustraction aboutit à un sous-dépassement d'entier (*underflow*), générant une valeur gigantesque transmise à une opération de copie mémoire. Cela entraîne un dépassement de tampon (*buffer overflow*) ou un crash immédiat du processus serveur.
* **Exploitabilité :** L'attaque nécessite environ 260 octets de trafic conforme aux spécifications. Aucun identifiant ni paquet malformé n'est requis. Bien qu'un crash soit démontré, la possibilité d'une exécution de code arbitraire n'a pas été confirmée.
* **État actuel :** La faille est présente depuis 2022. Il n'existe aucun correctif officiel ni identifiant CVE à ce jour, malgré plusieurs tentatives de divulgation responsable auprès d'Alibaba par les chercheurs de FoxIO.

**Vulnérabilité :**
* Non assignée (en attente de CVE).

**Recommandations :**
* Désactiver la table dynamique QPACK en configurant `SETTINGS_QPACK_MAX_TABLE_CAPACITY` à `0`.
* À défaut, suspendre temporairement la prise en charge du protocole HTTP/3 sur les serveurs utilisant XQUIC jusqu'à la publication d'un correctif.

---
[Source](https://thehackernews.com/2026/07/unpatched-xring-flaw-in-xquic-lets.html){:target="_blank"}
