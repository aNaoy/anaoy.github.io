---
title: 'Microsoft now lets admins uninstall Copilot on enterprise devices'
date: 2026-04-24
permalink: /posts/2026/04/24/microsoft-now-lets-admins-uninstall-copilot-on-enterprise-devices/
tags:
- veille-cyber
- bleepingcomp
---
### Désinstallation facilitée de Microsoft Copilot en entreprise

Microsoft offre désormais aux administrateurs informatiques la possibilité de désinstaller l'assistant IA Copilot sur les terminaux Windows 11 (version 25H2) via une nouvelle stratégie de groupe (`RemoveMicrosoftCopilotApp`). Cette option, intégrée aux mises à jour de sécurité d'avril 2026, permet une gestion centralisée des appareils via Intune ou SCCM pour les éditions Enterprise, Professional et Education.

**Points clés :**
* **Conditions d'application :** La désinstallation ne s'applique que si l'utilisateur n'a pas installé lui-même l'application et si celle-ci n'a pas été utilisée au cours des 28 derniers jours.
* **Flexibilité :** Bien que les administrateurs puissent supprimer l'application, les utilisateurs finaux conservent la possibilité de la réinstaller ultérieurement s'ils le souhaitent.
* **Changement de stratégie :** Microsoft réduit progressivement l'intégration forcée de fonctionnalités liées à l'IA au sein de Windows 11 pour limiter l'encombrement du système.

**Vulnérabilités :**
* Un bug identifié en février 2026 dans Microsoft 365 Copilot permettait à l'assistant de résumer des courriels confidentiels, contournant ainsi les politiques de prévention contre la perte de données (DLP). Aucune CVE n'a été spécifiquement mentionnée pour cet incident, mais il souligne les risques de confidentialité liés à l'IA générative en entreprise.

**Recommandations :**
* **Contrôle administratif :** Les administrateurs système doivent évaluer la pertinence de maintenir Copilot sur leurs parcs informatiques et utiliser la nouvelle stratégie `RemoveMicrosoftCopilotApp` via l'éditeur de stratégie de groupe pour standardiser les environnements de travail.
* **Gouvernance des données :** En raison des risques de contournement des politiques DLP par les outils d'IA, il est recommandé de renforcer la classification des données sensibles et de surveiller l'accès des assistants IA aux documents confidentiels.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-now-lets-admins-uninstall-copilot-on-enterprise-devices/){:target="_blank"}
