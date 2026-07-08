---
title: 'Microsoft to enable Windows settings backup by default for orgs'
date: 2026-07-08
permalink: /posts/2026/07/08/microsoft-to-enable-windows-settings-backup-by-default-for-orgs/
tags:
- veille-cyber
- bleepingcomp
---
### Automatisation de la sauvegarde des paramètres Windows en entreprise

À partir de Windows 11 version 26H2, Microsoft activera par défaut l'outil de sauvegarde des paramètres pour les systèmes joints à Microsoft Entra (ou Entra hybride). Cette fonctionnalité, initialement optionnelle, vise à simplifier la restauration des environnements utilisateurs lors du remplacement ou de la réinitialisation des postes de travail.

**Points clés :**
*   **Déploiement :** L'activation par défaut s'applique uniquement aux appareils dont la politique de sauvegarde n'a pas été explicitement configurée par les administrateurs.
*   **Contrôle administrateur :** Les politiques définies via Intune ou les objets de stratégie de groupe (GPO) prévalent sur ce comportement par défaut. Les administrateurs conservent la maîtrise totale du service.
*   **Restrictions géographiques et techniques :** La fonctionnalité n'est pas activée par défaut dans les pays régis par le *Digital Markets Act* (DMA) de l'UE, ni dans les environnements cloud souverains ou restreints.
*   **Restauration :** Contrairement à la sauvegarde, le processus de restauration des données ne sera pas activé par défaut et nécessitera toujours une configuration explicite par l'administration.

**Vulnérabilités :**
*   Aucune vulnérabilité (CVE) n'est associée à cette mise à jour. Il s'agit d'une évolution fonctionnelle de gestion des systèmes.

**Recommandations :**
*   **Audit des politiques :** Les administrateurs informatiques doivent vérifier si une configuration spécifique est déjà en place. Si la sauvegarde des données utilisateurs vers le cloud Microsoft n'est pas souhaitée, il est impératif de désactiver explicitement la politique via Microsoft Intune ou les GPO avant le déploiement de la version 26H2.
*   **Validation :** Il est possible de tester ce nouveau comportement via le programme *Windows Insider (Experimental Channel)* dès juillet 2026 afin d'évaluer l'impact sur les politiques de sécurité et de conformité de l'organisation.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-enable-windows-backup-for-organizations-by-default/){:target="_blank"}
