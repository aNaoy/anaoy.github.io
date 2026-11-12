---
title: 'Critical Red Hat Quay Flaw Lets Attackers Read and Overwrite All Private Container Images in a Registry'
date: 2026-11-12
permalink: /posts/2026/11/12/critical-red-hat-quay-flaw-lets-attackers-read-and-overwrite-all-private-container-images-in-a-registry/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques affectant Red Hat Quay

Deux failles critiques ont été identifiées dans Red Hat Quay, impactant l'ensemble des versions 3 et 5, y compris les déploiements sur OpenShift et les registres miroirs. Ces vulnérabilités permettent à des attaquants de compromettre l'intégrité et la confidentialité des images de conteneurs.

**Points clés :**
*   **CVE-2026-123710 (Score CVSS 9.8) :** Permet à un attaquant d'ajouter sa propre clé de confiance au serveur de clés de Quay sans date d'expiration. Cela lui donne un accès total pour lire, modifier ou écraser n'importe quelle image privée dans le registre, et d'injecter des images malveillantes dans les pipelines CI/CD.
*   **CVE-2026-110697 (Score CVSS 9.9) :** Une faille d'injection SQL dans la recherche de comptes "robot" permet à un utilisateur malveillant de voler les jetons (tokens) d'autres locataires (tenants) en créant des espaces de noms contenant des caractères génériques (underscore).
*   La désactivation de l'accès anonyme ne protège pas contre ces vecteurs d'attaque.

**Recommandations :**
1.  **Mise à jour :** Installer immédiatement les versions corrigées fournies par Red Hat.
2.  **Mitigation temporaire (CVE-2026-123710) :**
    *   Bloquer l'accès à l'endpoint `/keys` au niveau du proxy ou du load balancer pour tout client non interne.
    *   Auditer les logs pour détecter les événements `service_key_rotate` et `service_key_delete` avec une date d'expiration nulle.
    *   Supprimer toute clé de service non reconnue.
3.  **Mitigation temporaire (CVE-2026-110697) :**
    *   Restreindre la création d'espaces de noms contenant des underscores.
    *   Révoquer et renouveler les jetons des comptes "robot" pour les espaces de noms suspects.
    *   Surveiller les activités de "pull" et "push" anormales liées aux comptes "robot".

---
[Source](https://thehackernews.com/2026/11/critical-red-hat-quay-flaw-lets.html){:target="_blank"}
