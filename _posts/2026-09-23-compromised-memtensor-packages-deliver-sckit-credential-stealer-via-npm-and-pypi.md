---
title: 'Compromised MemTensor Packages Deliver sckit Credential Stealer via npm and PyPI'
date: 2026-09-23
permalink: /posts/2026/09/23/compromised-memtensor-packages-deliver-sckit-credential-stealer-via-npm-and-pypi/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement MemTensor : Le malware sckit

Des acteurs malveillants ont compromis des paquets légitimes du projet MemTensor sur les dépôts **npm** et **PyPI** pour déployer un implant malveillant baptisé **sckit**. Ce logiciel écrit en Go cible Windows, Linux et macOS afin de dérober des identifiants et des données sensibles sur les machines des développeurs et dans les pipelines CI/CD.

**Points clés :**
* **Méthode d'attaque :** Les assaillants ont récupéré les jetons de publication des paquets en manipulant les flux de travail (workflows) GitHub Actions de MemTensor.
* **Fonctionnalités du malware :** L'implant agit comme un ver capable de s'auto-propager, d'exécuter des tâches distantes reçues d'un serveur C2 (`skyleen.fr`) et d'infecter d'autres paquets ou workflows.
* **Cibles visées :** Le malware exfiltre une vaste gamme de secrets (AWS, GitHub, GitLab, Slack, Stripe, clés privées SSH, jetons npm/PyPI, variables d'environnement, etc.).

**Paquets compromis :**
* **npm :** `@memtensor/memos-cloud-openclaw-plugin` (versions 0.1.21, 0.1.23, 0.1.25).
* **PyPI :** `MemoryOS` (version 2.0.34).

**Vulnérabilités :**
Aucune CVE spécifique n'a été attribuée, car il s'agit d'une compromission directe des identifiants de publication (secrets de CI/CD) et d'une injection de code malveillant au sein de versions légitimes.

**Recommandations :**
* **Mise à jour immédiate :** Rétrograder ou verrouiller les paquets sur des versions saines (0.1.20 pour le paquet npm ; 2.0.33 pour le paquet PyPI).
* **Nettoyage :** Terminer tout processus actif lié à `sckit` sur les machines infectées.
* **Rotation des secrets :** Considérer comme compromis tous les jetons, clés API, mots de passe et identifiants présents sur les machines ou dans les environnements CI/CD ayant utilisé ces versions infectées.
* **Filtrage réseau :** Bloquer le domaine `skyleen.fr` ainsi que tous ses sous-domaines au niveau du pare-feu ou du proxy.

---
[Source](https://thehackernews.com/2026/09/compromised-memtensor-packages-deliver.html){:target="_blank"}
