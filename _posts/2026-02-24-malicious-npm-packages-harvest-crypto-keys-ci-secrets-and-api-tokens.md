---
title: 'Malicious npm Packages Harvest Crypto Keys, CI Secrets, and API Tokens'
date: 2026-02-24
permalink: /posts/2026/02/24/malicious-npm-packages-harvest-crypto-keys-ci-secrets-and-api-tokens/
tags:
- veille-cyber
- hackernews
---
### Vaste campagne de vol de secrets via des paquets npm malveillants

Une campagne active baptisée **SANDWORM_MODE** exploite au moins 19 paquets npm malveillants pour dérober des informations sensibles, notamment des clés de cryptomonnaie, des secrets d'intégration continue (CI) et des jetons d'API. Similaire aux attaques Shai-Hulud précédentes, ce ver de chaîne d'approvisionnement dérobe des informations système, des jetons d'accès, des secrets d'environnement et des clés d'API. Il se propage en utilisant des identifiants npm et GitHub volés.

Une fonctionnalité notable est le module "McpInject" qui cible les assistants de codage IA. Il déploie un serveur Model Context Protocol (MCP) malveillant et l'injecte dans les configurations des outils, utilisant des injections de prompt pour lire des fichiers sensibles comme `~/.ssh/id_rsa`, `~/.aws/credentials`, `.env`, et les clés d'API de neuf fournisseurs de LLM.

Le malware comprend également un moteur polymorphique conçu pour échapper à la détection en renommant des variables, en réécrivant le flux de contrôle et en ajoutant du code inutile. Bien que ce moteur soit désactivé dans les versions actuelles, sa présence suggère des futures itérations du malware.

L'attaque se déroule en deux étapes : la première capture les identifiants et les clés de cryptomonnaie, puis charge une seconde étape qui effectue une récolte plus approfondie, une propagation de type ver, l'injection MCP et une exfiltration complète. La seconde étape ne s'active qu'après un délai de 48 heures, avec une marge d'erreur supplémentaire.

**Points Clés :**

*   **Nature de la menace :** Ver de chaîne d'approvisionnement dérobant des secrets via des paquets npm.
*   **Ciblage :** Environnements de développement, assistants de codage IA, clés de cryptomonnaie, secrets CI/CD, jetons API.
*   **Mécanismes :** Utilisation de paquets npm malveillants, injection MCP pour cibler les IA, moteur polymorphique pour l'évasion, propagation via des identifiants volés.
*   **Latence :** L'activité malveillante la plus importante ne s'active qu'après une période de latence.

**Vulnérabilités / Vecteurs d'attaque :**

*   **Paquets npm malveillants :** Plus de 19 paquets identifiés, conçus pour semer le doute et la confusion (typosquatting).
*   **Action GitHub malveillante :** Permet l'exfiltration de secrets CI/CD.
*   **Injection de Prompt (MCP) :** Exploite les assistants de codage IA pour lire des fichiers sensibles.

**Recommandations :**

*   **Suppression immédiate :** Les utilisateurs ayant installé les paquets suspects doivent les désinstaller sans délai.
*   **Rotation des secrets :** Changer immédiatement tous les jetons npm, jetons GitHub et secrets CI/CD potentiellement compromis.
*   **Audit du code :** Examiner les fichiers `package.json`, les `lockfiles` et les workflows `.github/workflows/` pour toute modification suspecte.
*   **Vigilance accrue :** Traiter ces paquets comme des risques de compromission actifs.

---
[Source](https://thehackernews.com/2026/02/malicious-npm-packages-harvest-crypto.html){:target="_blank"}
