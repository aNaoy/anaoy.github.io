---
title: 'Critical Gitea Flaw Let Unauthenticated Attackers Read Server Files via Org-Mode Markup'
date: 2026-08-05
permalink: /posts/2026/08/05/critical-gitea-flaw-let-unauthenticated-attackers-read-server-files-via-org-mode-markup/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique de lecture de fichiers dans Gitea

Une faille critique affectant Gitea (versions 1.22.1 à 1.27.0) permet à un attaquant non authentifié de lire des fichiers arbitraires sur le serveur en exploitant le moteur de rendu de balisage Org-mode.

**Points clés :**
*   **Vecteur d'attaque :** L'attaquant envoie une requête `POST` vers le point de terminaison de rendu de balisage (`/markup`) en utilisant le format Org-mode. La directive `#+INCLUDE` permet d'accéder à des chemins de fichiers absolus sur le système de fichiers du serveur.
*   **Escalade potentielle :** Bien qu'il s'agisse d'une faille de lecture, elle peut mener à une exécution de code à distance (RCE) si l'attaquant récupère le fichier `app.ini`, dérobe le `INTERNAL_TOKEN` et injecte un hook Git malveillant.
*   **Conditions :** L'instance doit héberger au moins un dépôt public pour que l'attaque soit possible sans authentification.

**Vulnérabilités identifiées :**
*   **CVE-2026-59774 (Score CVSS 9.8) :** Faille critique de lecture arbitraire de fichiers via Org-mode.
*   **CVE-2026-60004 :** Vulnérabilité distincte d'exécution de code à distance (RCE) également corrigée dans la mise à jour 1.27.1.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **1.27.1** sans délai.
*   **Audit de sécurité post-exposition :** Si des traces d'accès suspectes aux points de terminaison `markup` sont détectées dans les logs :
    *   Considérer tous les secrets accessibles par le compte de service comme compromis (clés OAuth, JWT, identifiants de base de données).
    *   Procéder à une rotation systématique des jetons internes (`INTERNAL_TOKEN`).
    *   Inspecter les répertoires de hooks Git à la recherche de fichiers exécutables non autorisés.
*   **Surveillance :** Analyser les logs pour identifier des requêtes `POST` inhabituelles ciblant le rendu Org-mode ou contenant des chemins de fichiers absolus.

---
[Source](https://thehackernews.com/2026/08/critical-gitea-flaw-let-unauthenticated.html){:target="_blank"}
