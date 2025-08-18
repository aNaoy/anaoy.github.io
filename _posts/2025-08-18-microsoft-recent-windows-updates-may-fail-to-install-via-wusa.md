---
title: 'Microsoft: Recent Windows updates may fail to install via WUSA'
date: 2025-08-18
permalink: /posts/2025/08/18/microsoft-recent-windows-updates-may-fail-to-install-via-wusa/
tags:
- veille-cyber
- bleepingcomp
---
### Échec d'installation des mises à jour Windows via WUSA

Un problème connu affecte l'installation des mises à jour Windows sur les systèmes Windows 11 24H2 et Windows Server 2025 lorsqu'elles sont déployées à partir d'un partage réseau à l'aide de l'outil en ligne de commande WUSA (Windows Update Standalone Installer). Ce dysfonctionnement, qui survient spécifiquement lorsque le partage réseau contient plusieurs fichiers .msu, génère une erreur "ERROR_BAD_PATHNAME". Cette situation concerne les mises à jour déployées à partir du 28 mai 2025 (KB5058499) et versions ultérieures.

**Points clés :**

*   L'outil WUSA est utilisé par les administrateurs système pour installer et désinstaller des mises à jour Windows (.msu).
*   Le problème affecte les environnements d'entreprise utilisant des partages réseau.
*   L'erreur "ERROR_BAD_PATHNAME" est rencontrée lors de l'installation d'un package .msu depuis un partage contenant plusieurs fichiers .msu.
*   Les fichiers stockés localement ou les installations avec un seul fichier .msu ne sont pas concernés.

**Vulnérabilités (avec CVE si possible) :**

Aucune CVE n'est spécifiquement mentionnée dans l'article pour ce problème. Il s'agit d'un dysfonctionnement identifié dans le processus d'installation.

**Recommandations :**

*   **Pour les appareils grand public et non gérés :** Microsoft a corrigé ce problème via une mise à jour automatique par le biais de la fonction "Known Issue Rollback" (KIR).
*   **Pour les appareils gérés (par les entreprises) :** Les administrateurs peuvent résoudre ce problème en installant et configurant la mise à jour "Known Issue Rollback Group Policy" disponible pour Windows 11 24H2 et Windows Server 2022.
*   **Contournement manuel :** Il est possible de télécharger les fichiers .msu et de les enregistrer localement avant de lancer l'installation depuis cet emplacement.

L'article mentionne également d'autres problèmes d'installation de mises à jour rencontrés récemment par les administrateurs, notamment des erreurs 0x80240069 affectant Windows 11 22H2/23H2 et 24H2 lors du déploiement via WSUS.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-11-windows-server-2025-updates-may-fail-from-network-shares/){:target="_blank"}
