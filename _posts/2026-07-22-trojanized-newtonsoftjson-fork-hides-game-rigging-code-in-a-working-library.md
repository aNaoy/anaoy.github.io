---
title: 'Trojanized Newtonsoft.Json Fork Hides Game-Rigging Code in a Working Library'
date: 2026-07-22
permalink: /posts/2026/07/22/trojanized-newtonsoftjson-fork-hides-game-rigging-code-in-a-working-library/
tags:
- veille-cyber
- hackernews
---
### Attaque par typosquatting ciblant la plateforme de paris Digitain

Des chercheurs ont identifié un package NuGet malveillant nommé `Newtonsoftt.Json.Net`, se faisant passer pour la bibliothèque populaire `Newtonsoft.Json`. Ce package "typosquatté" contient une version cheval de Troie conçue pour manipuler les résultats du jeu de pari en ligne *FG-Crash* de la plateforme Digitain.

**Points clés :**
* **Ciblage chirurgical :** Le package fonctionne normalement pour la plupart des développeurs, dissimulant sa malveillance. Il ne s'active que sur les serveurs exécutant le backend spécifique du jeu de Digitain.
* **Évolution du malware :** Le code a évolué sur sept versions (11.0.4 à 11.0.11), passant d'une preuve de concept locale à un outil automatisé exfiltrant les résultats truqués vers un serveur distant.
* **Accès interne :** Les métadonnées du package révèlent une fuite d'URL interne, suggérant que l'attaquant a eu accès au code source du backend de la victime.
* **Discrétion :** Le malware utilise un délai aléatoire pour éviter la détection et masque ses communications avec le serveur de contrôle en les faisant passer pour des données de télémétrie.

**Vulnérabilités :**
* Il ne s'agit pas d'une vulnérabilité CVE classique, mais d'une **attaque par typosquatting** sur la chaîne d'approvisionnement logicielle, exploitant la confiance des développeurs dans les noms de packages similaires.

**Recommandations :**
* **Suppression immédiate :** Identifier et supprimer toute dépendance au package `Newtonsoftt.Json.Net` dans les projets.
* **Verrouillage des versions :** Utiliser des fichiers de verrouillage (`packages.lock.json`) pour garantir l'intégrité des bibliothèques installées et éviter les injections malveillantes.
* **Filtrage réseau :** Bloquer le trafic sortant vers l'adresse IP associée au serveur de contrôle : `185.126.237[.]64`.
* **Audit de sécurité :** Vérifier systématiquement les noms des packages dans les fichiers de configuration (NuGet/npm) pour détecter les variantes typosquattées.

---
[Source](https://thehackernews.com/2026/07/trojanized-newtonsoftjson-fork-hides.html){:target="_blank"}
