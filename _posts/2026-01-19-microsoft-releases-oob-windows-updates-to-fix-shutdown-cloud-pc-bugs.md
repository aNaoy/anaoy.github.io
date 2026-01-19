---
title: 'Microsoft releases OOB Windows updates to fix shutdown, Cloud PC bugs'
date: 2026-01-19
permalink: /posts/2026/01/19/microsoft-releases-oob-windows-updates-to-fix-shutdown-cloud-pc-bugs/
tags:
- veille-cyber
- bleepingcomp
---
**Mises à jour d'urgence pour Windows : Correction des problèmes d'accès Cloud PC et d'extinction**

Microsoft a déployé des mises à jour exceptionnelles pour Windows 10, Windows 11 et Windows Server afin de résoudre deux problèmes introduits par les correctifs de janvier.

**Points clés :**

*   **Problème 1 :** Blocage d'accès aux sessions Microsoft 365 Cloud PC et échec des invites d'identification dans les applications de connexion à distance. Ce problème affecte Windows 11, Windows 10 et Windows Server.
*   **Problème 2 :** Incapacité pour certains PC avec Secure Launch activé de s'éteindre ou d'entrer en hibernation ; les appareils redémarrent à la place. Ce problème concerne spécifiquement Windows 11 version 23H2.

**Vulnérabilités :**

Aucun identifiant CVE spécifique n'est mentionné dans l'article pour ces problèmes.

**Recommandations :**

*   **Installations manuelles :** Les mises à jour hors bande (OOB) corrigent ces problèmes. Elles ne sont pas disponibles via Windows Update et doivent être téléchargées et installées manuellement depuis le catalogue Microsoft Update. Les mises à jour spécifiques sont listées par version de Windows avec leurs KB associées (par exemple, KB5077797 pour Windows 11 23H2).
*   **Solution de contournement pour les entreprises :** Les administrateurs d'entreprise peuvent déployer un "Known Issue Rollback" (KIR) via la stratégie de groupe (Group Policy) pour résoudre le problème d'accès au Cloud PC si l'installation des mises à jour OOB n'est pas immédiate. Des liens de téléchargement pour les KIR sont fournis pour différentes versions de Windows.
*   **Attente des mises à jour régulières :** Si les problèmes n'affectent pas vos appareils, il est possible d'attendre les prochaines mises à jour prévues (aperçu ou Patch Tuesday du mois suivant).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-oob-windows-updates-to-fix-shutdown-cloud-pc-bugs/){:target="_blank"}
