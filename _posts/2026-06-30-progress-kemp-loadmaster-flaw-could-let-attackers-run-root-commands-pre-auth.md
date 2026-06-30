---
title: 'Progress Kemp LoadMaster Flaw Could Let Attackers Run Root Commands Pre-Auth'
date: 2026-06-30
permalink: /posts/2026/06/30/progress-kemp-loadmaster-flaw-could-let-attackers-run-root-commands-pre-auth/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique d'exécution de code à distance dans Progress Kemp LoadMaster

Une faille critique de sécurité affecte les répartiteurs de charge (load balancers) Progress Kemp LoadMaster, permettant à un attaquant non authentifié d'exécuter des commandes arbitraires avec les privilèges root.

**Points clés :**
*   **Mécanisme de la faille :** La vulnérabilité réside dans une mauvaise gestion de la mémoire lors de la désinfection des entrées utilisateur (fonction `escape_quotes()`). L'absence de caractère de terminaison nul dans un tampon mémoire permet à l'attaquant d'accéder à des données adjacentes et d'injecter des charges utiles de commande via des requêtes API JSON.
*   **Vecteur d'attaque :** L'exploitation cible le point de terminaison `/accessv2`. Aucun identifiant n'est requis.
*   **Disponibilité du PoC :** Bien qu'aucune exploitation active ne soit signalée, une preuve de concept (PoC) fonctionnelle a été publiée par des chercheurs, augmentant le risque d'attaques imminentes.

**Vulnérabilités :**
*   **CVE-2026-8037 (Score CVSS 9.8) :** Exécution de code à distance (RCE) pré-authentification via l'API.
*   **CVE-2026-33691 :** Contournement du pare-feu d'application Web (WAF) via des espaces dans les noms de fichiers lors du téléchargement.

**Recommandations :**
*   **Appliquer les correctifs :** Mettre à jour immédiatement vers les versions **GA v7.2.63.2** ou **LTSF v7.2.54.18**.
*   **Réduire la surface d'exposition :** Évaluer la nécessité d'exposer l'API de l'équipement sur le réseau. Si son usage n'est pas requis, désactivez-la ou restreignez-en strictement l'accès.

---
[Source](https://thehackernews.com/2026/06/progress-kemp-loadmaster-flaw-could-let.html){:target="_blank"}
