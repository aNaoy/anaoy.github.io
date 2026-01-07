---
title: 'Max severity Ni8mare flaw lets hackers hijack n8n servers'
date: 2026-01-07
permalink: /posts/2026/01/07/max-severity-ni8mare-flaw-lets-hackers-hijack-n8n-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Ni8mare : Une faille critique affectant N8N**

Une vulnérabilité de sévérité maximale, baptisée "Ni8mare", permet à des attaquants distants non authentifiés de prendre le contrôle d'instances déployées localement de la plateforme d'automatisation de flux de travail N8N. Cette faille, identifiée sous la référence CVE-2026-21858, a reçu une note de criticité de 10 sur 10. Les chercheurs estiment qu'il existe plus de 100 000 serveurs N8N vulnérables.

N8N est un outil open-source permettant de connecter des applications, des API et des services pour créer des flux de travail automatisés, avec une utilisation notable dans le domaine de l'intelligence artificielle pour orchestrer des appels aux modèles linguistiques et gérer des pipelines de données.

**Points Clés :**

*   **Nature de la faille :** Ni8mare exploite une confusion dans le traitement du type de contenu ('content-type') par N8N lors de la réception de requêtes de webhook. Normalement, lorsque le type est `multipart/form-data`, N8N utilise un analyseur spécial pour les téléversements de fichiers. Cependant, en spécifiant un autre type de contenu, comme `application/json`, un attaquant peut tromper N8N. L'outil traite alors des champs liés aux fichiers sans vérifier qu'il s'agit d'un véritable téléversement, permettant ainsi de contrôler les métadonnées du fichier, y compris le chemin.
*   **Impact :** Cette manipulation permet aux attaquants de lire des fichiers arbitraires sur le système hôte de N8N. Cela peut conduire à l'exposition d'informations sensibles stockées sur l'instance, telles que des clés API, des identifiants de base de données, des jetons OAuth, ou des secrets CI/CD. L'attaquant peut également injecter des fichiers dans les flux de travail, usurper des cookies de session pour contourner l'authentification, voire exécuter des commandes arbitraires.
*   **Importance de N8N :** N8N étant souvent configuré comme un hub central d'automatisation, il contient une quantité significative de données sensibles, rendant cette vulnérabilité particulièrement dangereuse.

**Vulnérabilités :**

*   **Nom :** Ni8mare
*   **Référence CVE :** CVE-2026-21858
*   **Score de sévérité :** 10/10 (critique)
*   **Type :** Confusion de type de contenu permettant l'accès aux fichiers et l'exécution de code à distance.

**Recommandations :**

*   **Mise à jour :** La mesure recommandée est de mettre à jour N8N vers la version 1.121.0 ou une version ultérieure.
*   **Atténuation temporaire :** En l'absence de correctif officiel immédiat pour les versions antérieures, il est conseillé de restreindre ou de désactiver les points d'accès webhook et les formulaires accessibles publiquement.

---
[Source](https://www.bleepingcomputer.com/news/security/max-severity-ni8mare-flaw-lets-hackers-hijack-n8n-servers/){:target="_blank"}
