---
title: 'Official Claude Code Extension on Cursor Marketplace Trojanized with Persistent SSH Backdoor'
date: 2026-10-30
permalink: /posts/2026/10/30/official-claude-code-extension-on-cursor-marketplace-trojanized-with-persistent-ssh-backdoor/
tags:
- veille-cyber
- hackernews
---
### Compromission de l'extension Claude Code sur le marketplace Cursor

Une version piégée de l'extension officielle Claude Code (v2.1.313) a été distribuée via le marketplace de l'IDE Cursor, affectant environ 5 000 utilisateurs. Bien que l'extension usurpait l'identité de l'éditeur légitime, elle contenait un script malveillant capable d'exfiltrer des informations système et d'établir une porte dérobée persistante.

**Points clés :**
*   **Propagation :** La compromission est limitée au marketplace de Cursor. Les marketplaces officiels VS Code et Open VSX ne sont pas impactés.
*   **Méthode d'attaque :** Un chargeur malveillant inséré dans le bundle JavaScript ajoute une clé SSH non autorisée (`svc-telemetry`) dans le fichier `~/.ssh/authorized_keys` de la victime.
*   **Exfiltration :** Le malware collecte des données système (nom d'hôte, IP, variables d'environnement liées aux secrets comme AWS ou GCP) et les transmet via une requête HTTP non chiffrée vers l'adresse IP `134.209.82.225`.
*   **Persistance :** Le logiciel malveillant installe des tâches planifiées, des crontabs ou des LaunchAgents selon l'OS (Windows, Linux, macOS).
*   **Accès distant :** Le malware tente d'établir un tunnel SSH inverse, bien que l'accès effectif soit limité par le besoin de privilèges administrateur pour activer le service SSH sur certains systèmes.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, il s'agit d'une attaque par **Supply Chain (chaîne d'approvisionnement)** visant un marketplace d'extensions.

**Recommandations :**
*   **Mise à jour :** Assurez-vous d'utiliser la version 2.1.314 (ou supérieure) fournie par Anthropic.
*   **Nettoyage :** Supprimer manuellement la clé SSH intitulée `svc-telemetry` du fichier `~/.ssh/authorized_keys`.
*   **Suppression des persistances :** Rechercher et supprimer les tâches planifiées ou processus suspects installés récemment.
*   **Rotation des secrets :** Considérant que des noms de variables d'environnement sensibles ont pu être exfiltrés, il est impératif de révoquer et de renouveler tous les jetons, clés API et identifiants potentiellement compromis.

---
[Source](https://thehackernews.com/2026/10/official-claude-code-vs-code-extension.html){:target="_blank"}
