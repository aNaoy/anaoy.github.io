---
title: 'Over 400 Arch Linux packages compromised to push rootkit, infostealer'
date: 2026-06-12
permalink: /posts/2026/06/12/over-400-arch-linux-packages-compromised-to-push-rootkit-infostealer/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission massive de paquets AUR par un rootkit et un infostealer

Plus de 400 paquets de l'Arch User Repository (AUR) ont été compromis via l'usurpation d'identité de mainteneurs de confiance ou le détournement de paquets orphelins. Les attaquants ont modifié les scripts `PKGBUILD` pour injecter un logiciel malveillant nommé `atomic-lockfile` lors de l'installation.

**Points clés :**
* **Vecteur d'attaque :** Utilisation de scripts post-installation pour télécharger et exécuter un paquet npm malveillant.
* **Cibles :** Développeurs et environnements de build (postes de travail).
* **Fonctionnalités malveillantes :** 
    * **Rootkit :** Utilisation de la technologie eBPF (extended Berkeley Packet Filter) pour obtenir des privilèges noyau, dissimuler des processus, des fichiers et des interfaces réseau.
    * **Infostealer :** Exfiltration massive de données sensibles (identifiants GitHub, jetons Vault, clés SSH, cookies de navigateur, données Slack/Discord/Teams).

**Vulnérabilités :**
* Aucune CVE n'est attribuée à ce jour, car il s'agit d'une campagne de type **supply-chain attack** (attaque par empoisonnement de la chaîne d'approvisionnement logicielle) exploitant la nature non vérifiée des dépôts communautaires AUR.

**Recommandations :**
* **Vérification :** Utiliser les scripts d'analyse disponibles sur GitHub pour détecter la présence de `atomic-lockfile` sur le système.
* **Réaction en cas d'infection :** En raison de la persistance offerte par le rootkit, une réinstallation complète du système est fortement recommandée.
* **Hygiène de sécurité :** Révoquer et renouveler immédiatement toutes les informations d'identification potentiellement compromises (clés SSH, tokens, mots de passe).
* **Bonnes pratiques :** Privilégier les paquets issus de projets maintenus activement et auditer systématiquement les scripts `PKGBUILD` avant toute installation depuis l'AUR.

---
[Source](https://www.bleepingcomputer.com/news/security/over-400-arch-linux-packages-compromised-to-push-rootkit-infostealer/){:target="_blank"}
