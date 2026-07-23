---
title: 'Attackers Weaponize GitHub Actions Runners to Target cPanel and WHM Servers'
date: 2026-07-23
permalink: /posts/2026/07/23/attackers-weaponize-github-actions-runners-to-target-cpanel-and-whm-servers/
tags:
- veille-cyber
- hackernews
---
### Détournement de GitHub Actions pour cibler les serveurs cPanel et WHM

Une campagne malveillante utilise des dépôts GitHub compromis pour transformer l'infrastructure de GitHub Actions en une plateforme d'attaque distribuée. En injectant des flux de travail (workflows) malveillants dans des bibliothèques PHP légitimes (notamment sur Packagist), les attaquants utilisent des exécuteurs GitHub pour scanner et exploiter des serveurs cPanel et WHM vulnérables à travers le monde.

**Points clés :**
* **Méthode d'attaque :** Utilisation de dépôts légitimes compromis pour déployer des centaines de fichiers YAML de GitHub Actions.
* **Cible :** Serveurs cPanel et WHM vulnérables pour le vol de données sensibles (clés API cloud, accès base de données, jetons Git, identifiants SSH, etc.).
* **Ampleur :** Plus de 6 100 fichiers de workflow malveillants identifiés, partageant un identifiant DNS unique, suggérant une campagne automatisée à grande échelle.
* **Infrastructures :** Les exécuteurs GitHub téléchargent des charges utiles depuis un serveur de commande et contrôle (C2) situé à l'adresse `43.228.157[.]68`.

**Vulnérabilité exploitée :**
* **CVE-2026-41940 :** Vulnérabilité de contournement d'authentification dans cPanel et WHM permettant une prise de contrôle à distance.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs de sécurité pour cPanel et WHM afin de remédier à la vulnérabilité CVE-2026-41940.
* **Audit des dépendances :** Surveiller les bibliothèques tierces intégrées aux projets, particulièrement celles dont les versions de développement ont été modifiées récemment.
* **Sécurisation des comptes :** Renforcer les mesures de sécurité sur les comptes de maintenance de dépôts (authentification multi-facteurs, rotation des jetons d'accès).
* **Surveillance des workflows :** Auditer régulièrement les fichiers GitHub Actions au sein des dépôts pour détecter toute automatisation non autorisée ou suspecte.

---
[Source](https://thehackernews.com/2026/07/attackers-weaponize-github-actions.html){:target="_blank"}
