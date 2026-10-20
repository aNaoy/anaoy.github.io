---
title: 'OVHcloud CLI releases backdoored on GitHub to steal developer secrets'
date: 2026-10-20
permalink: /posts/2026/10/20/ovhcloud-cli-releases-backdoored-on-github-to-steal-developer-secrets/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission des versions CLI d'OVHcloud par le groupe GlassWorm

Des attaquants ont compromis le compte GitHub d'un développeur pour injecter un logiciel malveillant dans les versions 0.11.0 à 0.15.0 de l'outil en ligne de commande (CLI) d'OVHcloud. L'incident, attribué à la campagne "GlassWorm", visait à dérober des secrets stockés localement sur les machines des utilisateurs.

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'un compte développeur GitHub compromis depuis plusieurs mois pour modifier directement les releases existantes en contournant les processus de CI/CD.
* **Cibles :** Utilisateurs ayant téléchargé les versions v0.11.0 à v0.15.0 sur macOS, Linux et Windows.
* **Impact :** Vol de secrets (identifiants, clés API, jetons) présents sur le disque de la machine infectée.
* **Intégrité :** Les versions 0.10.0 et 0.16.0, ainsi que les images Docker et les compilations depuis la source, ne sont pas affectées.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, l'attaque reposant sur une mauvaise configuration de sécurité : l'option « release immutability » (immuabilité des versions) était désactivée sur le dépôt GitHub, permettant de remplacer des binaires légitimes par des versions malveillantes sans validation supplémentaire.

**Recommandations :**
* **Nettoyage système :** Si vous avez exécuté l'une des versions compromises, considérez que tous les secrets présents sur votre machine sont compromis.
* **Réinitialisation :** Révoquez et régénérez immédiatement toutes les clés, mots de passe et jetons d'accès stockés sur les systèmes ayant utilisé ces versions du CLI.
* **Mise à jour :** Mettez à jour vers la version 0.16.0 ou supérieure.
* **Sécurité dépôt :** Pour les mainteneurs de projets, activez systématiquement l'option "Release Immutability" sur GitHub afin d'empêcher toute modification non autorisée des artefacts publiés.

---
[Source](https://www.bleepingcomputer.com/news/security/ovhcloud-cli-releases-backdoored-on-github-to-steal-developer-secrets/){:target="_blank"}
