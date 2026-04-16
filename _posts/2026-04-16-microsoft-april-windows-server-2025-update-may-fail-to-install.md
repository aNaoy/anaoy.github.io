---
title: 'Microsoft: April Windows Server 2025 update may fail to install'
date: 2026-04-16
permalink: /posts/2026/04/16/microsoft-april-windows-server-2025-update-may-fail-to-install/
tags:
- veille-cyber
- bleepingcomp
---
### Problèmes d'installation et de démarrage sur Windows Server 2025

Microsoft enquête actuellement sur des échecs d'installation affectant la mise à jour de sécurité KB5082063 sur certains systèmes Windows Server 2025.

**Points clés :**
*   **Erreur d'installation :** Un nombre limité de serveurs rencontre l'erreur `0x800F0983` lors du déploiement des mises à jour cumulatives d'avril 2026.
*   **Blocage BitLocker :** La mise à jour KB5082063 provoque, sur certaines configurations d'entreprise, un redémarrage en mode de récupération BitLocker, exigeant la saisie d'une clé de déverrouillage.
*   **Résolution de mise à niveau forcée :** Microsoft a corrigé le bug persistant qui provoquait des migrations inattendues de Windows Server 2019 et 2022 vers Windows Server 2025.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée pour ces erreurs d'installation.

**Recommandations :**
*   **Surveillance :** Les administrateurs système doivent suivre les alertes de service Microsoft (WI1281095) pour obtenir des mises à jour sur le diagnostic de la cause racine.
*   **Gestion des clés :** En cas de déploiement en environnement d'entreprise, assurez-vous que les clés de récupération BitLocker sont accessibles et sauvegardées avant d'appliquer les correctifs de sécurité.
*   **Attente :** Dans l'attente d'un correctif officiel ou d'une clarification de la part de Microsoft, il est conseillé de tester la mise à jour sur un périmètre restreint avant une généralisation à l'ensemble du parc serveur.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-april-windows-server-2025-update-may-fail-to-install/){:target="_blank"}
