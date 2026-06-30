---
title: '282 iOS AI Apps Leak API Keys and Open AI Proxy Access in Network Traffic Study'
date: 2026-06-30
permalink: /posts/2026/06/30/282-ios-ai-apps-leak-api-keys-and-open-ai-proxy-access-in-network-traffic-study/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les applications iOS intégrant l'IA

Une étude menée sur 444 applications iOS utilisant l'intelligence artificielle a révélé que près de 64 % d'entre elles (282 applications) exposent des clés d'API ou des accès aux services d'IA via leur trafic réseau, sans nécessiter de techniques de piratage sophistiquées. Cette faille facilite le « LLMjacking », permettant à des attaquants d'utiliser les ressources d'IA aux frais des développeurs.

**Points clés :**
*   **Méthode de découverte :** L'outil *LLMKeyLens* a permis d'extraire des identifiants en interceptant simplement le trafic réseau des applications.
*   **Vecteurs d'exposition :** 
    *   **Clés en clair :** Identifiants visibles directement dans les requêtes (54 apps).
    *   **Relais ouverts :** Serveurs backend acceptant les requêtes sans aucune authentification (92 apps).
    *   **Jetons réutilisables :** Jetons d'accès censés être temporaires mais souvent valides sur le long terme, voire quasi indéfiniment (136 apps).
*   **Dommages collatéraux :** En plus des clés d'API, certaines requêtes exposent des instructions système (« system prompts ») propriétaires.
*   **Réactivité :** Trois mois après la notification, seuls 28 % des développeurs avaient corrigé leurs vulnérabilités.

**Vulnérabilités :**
Bien qu'il n'existe pas de numéro CVE spécifique unique, ces problèmes relèvent de failles de conception critiques :
*   **Exposition d'informations sensibles (CWE-200) :** Transmission de secrets d'authentification en clair ou via des jetons mal sécurisés.
*   **Gestion inappropriée de l'authentification (CWE-287) :** Absence de vérification côté serveur des requêtes envoyées aux modèles d'IA.

**Recommandations :**
*   **Côté développeurs :** Ne jamais intégrer de clés d'API directement dans le code source de l'application. Toutes les requêtes vers les services d'IA doivent impérativement transiter par un serveur intermédiaire sécurisé qui authentifie l'utilisateur avant de transmettre la requête au fournisseur d'IA.
*   **Côté fournisseurs d'IA :** Mettre en place des mécanismes de détection d'anomalies pour identifier et révoquer automatiquement les clés utilisées simultanément par des milliers d'appareils ou de manière inhabituelle.
*   **Côté Apple :** Renforcer le processus de validation sur l'App Store pour détecter systématiquement l'inclusion de clés API ou de jetons sensibles dans les binaires des applications.

---
[Source](https://thehackernews.com/2026/06/282-ios-apps-found-leaking-llm-api-keys.html){:target="_blank"}
