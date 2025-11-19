---
title: 'Cloudflare blames this weeks massive outage on database issues'
date: 2025-11-19
permalink: /posts/2025/11/19/cloudflare-blames-this-weeks-massive-outage-on-database-issues/
tags:
- veille-cyber
- bleepingcomp
---
**Incident Majeur chez Cloudflare : Dysfonctionnement d'une Mise à Jour des Bases de Données**

Un incident majeur a affecté Cloudflare, entraînant une interruption de service de près de six heures, la plus importante depuis six ans. Cette panne généralisée a impacté de nombreux sites web et plateformes en ligne à travers le monde. Le déclencheur de cette cascade de défaillances a été une modification des contrôles d'accès à une base de données.

**Causes de l'Incident :**

*   **Modification des Permissions de Base de Données :** Une mise à jour des permissions de la base de données a conduit le système de gestion des robots (Bot Management) de Cloudflare à générer un fichier de configuration excessivement volumineux et contenant des doublons.
*   **Dépassement des Limites Système :** Ce fichier, en raison de ses doublons et de sa taille, a dépassé les limites prédéfinies du système, provoquant le crash du logiciel responsable du routage du trafic.
*   **Problèmes de Code :** Le code Rust du module de gestion des robots a rencontré une erreur système (panic) lors de la propagation du fichier problématique sur les machines du réseau, entraînant des erreurs 5xx et l'arrêt du système de proxy principal.
*   **Instabilité du Réseau :** Des requêtes de base de données erronées, générées toutes les cinq minutes, causaient des fluctuations entre des états fonctionnels et défaillants du réseau.

**Impact :**

L'incident a perturbé les services essentiels de Cloudflare, notamment le réseau de diffusion de contenu (CDN), les services de sécurité, Turnstile, Workers KV, l'accès au tableau de bord, la sécurité par e-mail et l'authentification.

**Recommandations (Implicites) :**

Bien qu'aucun numéro CVE spécifique ne soit mentionné dans l'article pour cette vulnérabilité interne, les leçons tirées de cet incident suggèrent la nécessité de :

*   **Tests Rigoureux des Mises à Jour :** Examiner minutieusement les changements apportés aux contrôles d'accès aux bases de données et aux configurations système avant leur déploiement en production.
*   **Gestion des Limites de Taille :** S'assurer que les systèmes sont conçus pour gérer des fichiers de configuration potentiellement volumineux et que les limites de taille sont correctement configurées et surveillées.
*   **Surveillance Renforcée :** Mettre en place des mécanismes de surveillance plus robustes pour détecter rapidement les anomalies dans la génération de fichiers de configuration et les erreurs système.
*   **Stratégies de Rollback Efficaces :** Disposer de procédures de retour arrière rapides et fiables pour rétablir des versions stables en cas de problème.

Cloudflare a précisé que cet incident n'était pas le résultat d'une cyberattaque.

---
[Source](https://www.bleepingcomputer.com/news/technology/cloudflare-blames-this-weeks-massive-outage-on-database-issues/){:target="_blank"}
