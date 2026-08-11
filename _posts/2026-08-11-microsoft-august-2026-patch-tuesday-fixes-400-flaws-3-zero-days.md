---
title: 'Microsoft August 2026 Patch Tuesday fixes 400 flaws, 3 zero-days'
date: 2026-08-11
permalink: /posts/2026/08/11/microsoft-august-2026-patch-tuesday-fixes-400-flaws-3-zero-days/
tags:
- veille-cyber
- bleepingcomp
---
### Patch Tuesday Août 2026 : 400 vulnérabilités corrigées

Microsoft a publié son cycle de mises à jour de sécurité pour août 2026, corrigeant un total de 400 vulnérabilités. Ce déploiement inclut 42 failles classées "Critiques", dont 37 concernent l'exécution de code à distance (RCE) et 5 l'élévation de privilèges.

#### Points clés
*   **Volumétrie :** 400 vulnérabilités traitées.
*   **Zero-days :** 3 failles zero-day ont été corrigées, dont une exploitée activement.
*   **Stratégie de détection :** Microsoft signale une augmentation du volume de correctifs, conséquence de l'intégration croissante de systèmes de découverte de vulnérabilités basés sur l'IA.

#### Vulnérabilités Zero-Day identifiées
1.  **CVE-2026-68820 (Exploitée activement) :** Vulnérabilité d'élévation de privilèges (SYSTEM) dans le pilote *Windows Ancillary Function Driver for WinSock* (AFD.sys). Elle a été utilisée par le groupe Lazarus pour déployer le rootkit *FudModule*.
2.  **Service de profil utilisateur Windows :** Vulnérabilité d'élévation de privilèges vers le niveau administrateur due à une résolution de lien incorrecte. Correspond aux détails de la faille "LegacyHive".
3.  **Pilote de filtrage du système de fichiers d'isolation des conteneurs (unionfs.sys) :** Faille d'élévation de privilèges locale permettant l'accès ou la modification des données d'autres utilisateurs.

#### Recommandations
*   **Appliquer les correctifs :** Il est impératif de déployer les mises à jour de sécurité de ce mois-ci, en priorité sur les systèmes exposés (Windows, serveurs Exchange, Azure, Office).
*   **Surveillance :** Étant donné l'exploitation active de `CVE-2026-68820` par des acteurs étatiques pour installer des rootkits, une inspection des journaux système et une recherche de comportements anormaux au niveau du noyau sont recommandées.
*   **Gestion des accès :** Compte tenu de la criticité des failles d'élévation de privilèges, limiter les droits des utilisateurs locaux et surveiller les processus accédant aux ruches de registre.

Le rapport complet, incluant la liste exhaustive des CVE et les produits concernés (dont .NET, Active Directory, Azure, Office, SharePoint et Windows), est disponible via le guide de mise à jour de Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-august-2026-patch-tuesday-fixes-400-flaws-3-zero-days/){:target="_blank"}
