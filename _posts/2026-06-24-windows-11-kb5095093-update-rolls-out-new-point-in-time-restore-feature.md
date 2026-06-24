---
title: 'Windows 11 KB5095093 update rolls out new Point-in-Time restore feature'
date: 2026-06-24
permalink: /posts/2026/06/24/windows-11-kb5095093-update-rolls-out-new-point-in-time-restore-feature/
tags:
- veille-cyber
- bleepingcomp
---
### Déploiement de la mise à jour Windows 11 KB5095093 : Nouvelles fonctionnalités et correctifs

La mise à jour optionnelle **KB5095093** pour Windows 11 (versions 24H2 et 25H2) introduit plusieurs améliorations système et correctifs fonctionnels. Bien qu'il s'agisse d'une version préliminaire sans correctifs de sécurité critiques, elle prépare le terrain pour les futures mises à jour obligatoires.

#### Points clés
*   **Point-in-Time Restore :** Nouvelle fonctionnalité de récupération système permettant de restaurer l'état complet du PC (fichiers, applications, paramètres) via des clichés VSS sur une période de 72 heures.
*   **Améliorations réseau et authentification :** Renforcement des connexions Netlogon, optimisation de la stack réseau et meilleure gestion des connexions VPN pour WSL.
*   **Correctifs d'interface :** Résolution d'un bug affichant des noms de fichiers internes lors de la suppression dans la Corbeille et amélioration de la fiabilité de l'explorateur de fichiers.
*   **Optimisations diverses :** Mise à jour du panneau Emoji vers GIPHY, nouveaux contrôles pour les Widgets, options d'accessibilité (teinte d'écran, loupe) et meilleure prise en charge des modèles d'IA locaux pour les systèmes de plus de 32 Go de RAM.

#### Vulnérabilités et problèmes connus
*   **Problème non résolu :** Un dysfonctionnement persiste après l'installation, empêchant le lancement correct des applications Microsoft Office à partir de logiciels tiers.
*   **CVE :** Aucun identifiant CVE n'est associé à cette mise à jour, car elle ne contient pas de correctifs de sécurité.

#### Recommandations
*   **Installation :** Cette mise à jour est facultative. Elle peut être installée via Windows Update ou manuellement via le catalogue Microsoft Update pour tester les nouvelles fonctionnalités.
*   **Contournement temporaire :** En cas d'impossibilité de lancer Office via une application tierce, il est conseillé d'ouvrir directement les documents ou les logiciels concernés manuellement.
*   **Gestion de la récupération :** Pour les utilisateurs en entreprise, il est recommandé de configurer manuellement la fréquence des snapshots de "Point-in-Time Restore" (intervalles de 4h à 24h) et d'ajuster l'espace disque alloué selon les besoins de rétention.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5095093-update-rolls-out-new-point-in-time-restore-feature/){:target="_blank"}
