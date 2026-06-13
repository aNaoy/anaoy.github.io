---
title: 'Over 400 Arch Linux AUR Packages Hijacked to Deploy Infostealer and eBPF Rootkit'
date: 2026-06-13
permalink: /posts/2026/06/13/over-400-arch-linux-aur-packages-hijacked-to-deploy-infostealer-and-ebpf-rootkit/
tags:
- veille-cyber
- hackernews
---
### Compromission massive de paquets AUR : campagne "Atomic Arch"

Plus de 400 paquets de l'Arch User Repository (AUR) ont été détournés pour infecter les machines des utilisateurs avec un logiciel malveillant (infostealer). Les attaquants ont ciblé des paquets orphelins, en prenant le contrôle de leur maintenance pour modifier les scripts de construction (`PKGBUILD`). Cette attaque par chaîne d'approvisionnement exploite la confiance accordée à l'historique des paquets plutôt qu'une faille logicielle spécifique.

**Points clés :**
* **Méthode :** Utilisation de paquets NPM malveillants (`atomic-lockfile`, `js-digest`) injectés lors de la compilation pour télécharger et exécuter un binaire Rust.
* **Cibles :** Développeurs et administrateurs système (vol de tokens, clés SSH, identifiants Docker/VPN, cookies de navigateur et sessions d'applications comme Slack/Discord).
* **Persistance :** Installation via des services `systemd` (utilisateur ou système).
* **Rootkit :** Un rootkit eBPF est déployé uniquement si le script est exécuté avec les privilèges root, permettant de masquer les processus et fichiers malveillants.

**Vulnérabilités :**
* Aucun CVE assigné (l'attaque cible le modèle de confiance humain).
* Identifiant de campagne : **Sonatype-2026-003775** (Score CVSS estimé : 8.7).

**Recommandations :**
* **Audit immédiat :** Vérifier les paquets installés ou mis à jour depuis le 11 juin. Rechercher spécifiquement les commandes `npm install atomic-lockfile` ou `bun install js-digest` dans les fichiers `PKGBUILD`.
* **Réponse à incident :** Si un paquet compromis a été exécuté, considérer tous les identifiants présents sur la machine comme compromis et procéder à une rotation immédiate (mots de passe, jetons, clés SSH).
* **Réinstallation :** En cas d'exécution avec les privilèges root, la réinstallation complète du système depuis un support de confiance est impérative, le rootkit rendant l'intégrité du système indémontrable.
* **Prudence :** Inspecter systématiquement les fichiers `PKGBUILD` avant toute installation, particulièrement pour les paquets récemment adoptés ou ayant connu une période d'inactivité.

---
[Source](https://thehackernews.com/2026/06/over-400-arch-linux-aur-packages.html){:target="_blank"}
