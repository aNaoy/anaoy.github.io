---
title: 'Critical n8n Flaw (CVSS 9.9) Enables Arbitrary Code Execution Across Thousands of Instances'
date: 2025-12-23
permalink: /posts/2025/12/23/critical-n8n-flaw-cvss-99-enables-arbitrary-code-execution-across-thousands-of-instances/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilité Critique dans n8n : Exécution de Code Arbitraire**

Une faille de sécurité grave (CVSS 9.9) a été découverte dans la plateforme d'automatisation de flux de travail n8n, permettant l'exécution de code arbitraire.

**Points Clés :**

*   La vulnérabilité, identifiée comme **CVE-2025-68613**, affecte les versions de n8n antérieures à 1.120.4.
*   Elle permet à un utilisateur authentifié de manipuler des expressions lors de la configuration des flux de travail pour exécuter du code malveillant avec les privilèges du processus n8n.
*   Cela peut mener à une compromission totale de l'instance, incluant l'accès à des données sensibles, la modification des flux et l'exécution d'opérations système.
*   Environ 103 476 instances seraient potentiellement vulnérables, principalement situées aux États-Unis, en Allemagne, en France, au Brésil et à Singapour.

**Vulnérabilités :**

*   **CVE-2025-68613** : Exécution de code arbitraire via l'évaluation non isolée d'expressions fournies par des utilisateurs authentifiés.

**Recommandations :**

*   Appliquer les mises à jour vers les versions corrigées (1.120.4, 1.121.1, et 1.122.0) dès que possible.
*   Si la mise à jour immédiate n'est pas possible :
    *   Restreindre la création et la modification des flux de travail aux utilisateurs de confiance.
    *   Déployer n8n dans un environnement sécurisé avec des privilèges système et un accès réseau restreints.

---
[Source](https://thehackernews.com/2025/12/critical-n8n-flaw-cvss-99-enables.html){:target="_blank"}
