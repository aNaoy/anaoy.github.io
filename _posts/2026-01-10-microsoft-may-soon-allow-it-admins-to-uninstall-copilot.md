---
title: 'Microsoft may soon allow IT admins to uninstall Copilot'
date: 2026-01-10
permalink: /posts/2026/01/10/microsoft-may-soon-allow-it-admins-to-uninstall-copilot/
tags:
- veille-cyber
- bleepingcomp
---
**Contrôle Accru sur Copilot pour les Administrateurs IT**

Microsoft déploie une nouvelle fonctionnalité permettant aux administrateurs de systèmes de désinstaller l'assistant IA Copilot sur les appareils gérés. Cette option, nommée `RemoveMicrosoftCopilotApp`, est actuellement testée dans les canaux Dev et Beta Insider de Windows 11 (build 26220.7535). Elle s'applique aux appareils gérés via Microsoft Intune ou System Center Configuration Manager, sous certaines conditions : Copilot doit être installé, il ne doit pas l'avoir été par l'utilisateur final, et il n'a pas été utilisé dans les 28 derniers jours. La désinstallation est effectuée une seule fois, mais les utilisateurs conservent la possibilité de le réinstaller. Cette politique est disponible pour les éditions Enterprise, Pro et EDU de Windows. La procédure pour l'activer implique l'éditeur de stratégie de groupe, sous "Configuration utilisateur -> Modèles d'administration -> Windows AI -> Remove Microsoft Copilot App".

**Points Clés :**

*   Une nouvelle politique `RemoveMicrosoftCopilotApp` permet la désinstallation de Copilot.
*   Ceci est destiné aux appareils gérés par IT via Intune ou SCCM.
*   La fonctionnalité est en cours de déploiement dans les canaux Insider Dev et Beta.
*   Les utilisateurs conservent la possibilité de réinstaller Copilot.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans le texte concernant la fonctionnalité de désinstallation de Copilot.

**Recommandations :**

*   Pour les administrateurs IT : Utiliser la nouvelle politique `RemoveMicrosoftCopilotApp` pour gérer la présence de Copilot sur les appareils gérés.
*   Pour les utilisateurs : Si Copilot est désinstallé par l'IT, ils ont la possibilité de le réinstaller s'ils le souhaitent.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-may-soon-allow-it-admins-to-uninstall-copilot-on-managed-devices/){:target="_blank"}
