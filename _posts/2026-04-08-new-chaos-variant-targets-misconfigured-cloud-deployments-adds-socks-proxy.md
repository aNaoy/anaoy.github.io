---
title: 'New Chaos Variant Targets Misconfigured Cloud Deployments, Adds SOCKS Proxy'
date: 2026-04-08
permalink: /posts/2026/04/08/new-chaos-variant-targets-misconfigured-cloud-deployments-adds-socks-proxy/
tags:
- veille-cyber
- hackernews
---
### Évolution du botnet Chaos : Cible Cloud et Proxy SOCKS

Le logiciel malveillant **Chaos**, initialement axé sur les routeurs et les périphériques réseau, a évolué pour cibler spécifiquement les déploiements cloud mal configurés. Cette nouvelle variante, observée sur des instances Hadoop, démontre une mutation vers des services de proxy pour masquer les activités malveillantes.

**Points clés :**
* **Expansion des capacités :** Le malware a abandonné ses fonctions de propagation par force brute SSH et d'exploitation de vulnérabilités sur les routeurs au profit d'un module de **proxy SOCKS**.
* **Objectif stratégique :** Ce pivot permet aux attaquants de louer l'accès au réseau compromis (proxy) pour relayer des attaques, masquant ainsi l'origine réelle du trafic.
* **Origine probable :** L'utilisation d'infrastructures liées au groupe cybercriminel chinois « Silver Fox » suggère une origine similaire.
* **Mode opératoire :** L'attaque exploite une mauvaise configuration pour exécuter une requête HTTP créant une application malveillante, télécharge le binaire, lui donne des droits d'exécution complets (`chmod 777`), puis supprime les traces pour échapper à la détection.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais pointe une **mauvaise configuration critique** (ex: instances Hadoop non sécurisées) permettant l'exécution de code à distance (RCE).

**Recommandations :**
* **Audit de configuration :** Sécuriser les services cloud (notamment Hadoop, Docker et autres services d'infrastructure) en désactivant les accès distants non autorisés.
* **Principe du moindre privilège :** Restreindre les permissions d'exécution sur les serveurs pour empêcher l'exécution de binaires non approuvés.
* **Surveillance du trafic :** Mettre en place des outils de détection d'anomalies pour identifier les comportements de type proxy ou les connexions sortantes suspectes vers des domaines inconnus ou réputés malveillants.
* **Gestion de la surface d'attaque :** Supprimer les services exposés inutilement sur Internet et appliquer les correctifs de sécurité régulièrement pour éviter les exploitations post-configuration.

---
[Source](https://thehackernews.com/2026/04/new-chaos-variant-targets-misconfigured.html){:target="_blank"}
