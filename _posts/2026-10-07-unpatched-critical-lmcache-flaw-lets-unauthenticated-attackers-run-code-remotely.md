---
title: 'Unpatched Critical LMCache Flaw Lets Unauthenticated Attackers Run Code Remotely'
date: 2026-10-07
permalink: /posts/2026/10/07/unpatched-critical-lmcache-flaw-lets-unauthenticated-attackers-run-code-remotely/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code à distance dans LMCache

Une faille critique a été identifiée dans **LMCache**, un logiciel open-source utilisé pour optimiser les serveurs LLM (comme vLLM). Cette vulnérabilité permet à un attaquant non authentifié d'exécuter du code arbitraire sur le serveur de cache.

**Points clés :**
*   **Cause technique :** Le mode « multiprocess » de LMCache utilise la bibliothèque ZeroMQ pour communiquer, sans aucune authentification. Le serveur traite les messages entrants via le module Python `pickle`, qui exécute automatiquement le code contenu dans le message lors de sa désérialisation.
*   **Risque d'exécution :** Le code est exécuté avec les privilèges du processus LMCache. Sur les images de conteneurs officielles, ce processus s'exécute avec les privilèges **root**.
*   **Exposition :** La vulnérabilité est exploitée si le serveur est configuré pour écouter sur une adresse réseau routable (cas fréquent dans les déploiements Kubernetes). Par défaut, l'écoute est limitée à `localhost`, ce qui limite le risque.
*   **État actuel :** Aucune version corrective n'est disponible à ce jour.

**Vulnérabilités :**
*   **CVE-2026-105192 :** Score CVSS de 9.8/10 (Critique). Concerne les versions de 0.3.9 à 0.5.5, ainsi que les versions de développement.

**Recommandations :**
*   **Limiter l'exposition :** Ne pas configurer le serveur LMCache pour écouter sur des adresses IP routables. Maintenir le port sur `localhost` ou au sein d'un réseau de cluster strictement cloisonné.
*   **Firewall :** Utiliser un pare-feu pour restreindre l'accès au port de communication à des machines de confiance, bien que cette mesure soit considérée comme une atténuation insuffisante.
*   **Surveillance :** Être vigilant face à l'absence d'outils officiels pour détecter si une compromission a déjà eu lieu.

---
[Source](https://thehackernews.com/2026/10/unpatched-critical-lmcache-flaw-lets.html){:target="_blank"}
