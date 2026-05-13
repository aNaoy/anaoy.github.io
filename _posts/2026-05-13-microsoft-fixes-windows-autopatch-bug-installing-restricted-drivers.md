---
title: 'Microsoft fixes Windows Autopatch bug installing restricted drivers'
date: 2026-05-13
permalink: /posts/2026/05/13/microsoft-fixes-windows-autopatch-bug-installing-restricted-drivers/
tags:
- veille-cyber
- bleepingcomp
---
### Correction d'une faille dans Windows Autopatch pour l'Union européenne

Microsoft a corrigé un bug affectant le service Windows Autopatch qui contournait les politiques de gestion des pilotes. Ce problème permettait l'installation automatique de pilotes recommandés sur des appareils gérés, alors même que les administrateurs informatiques avaient configuré des restrictions exigeant une approbation manuelle.

**Points clés :**
* **Cible :** Appareils Windows 11 (versions 23H2, 24H2 et 25H2) situés dans l'Union européenne.
* **Impact :** Installation forcée de pilotes non approuvés, provoquant des redémarrages intempestifs et, dans certains cas, des défaillances du système.
* **Vulnérabilités :** Aucune CVE n'a été attribuée, le problème étant lié à une erreur de configuration côté service dans la logique de déploiement de Windows Autopatch.

**Recommandations :**
* Aucune action n'est requise de la part des administrateurs ou des utilisateurs. Le correctif a été appliqué directement par Microsoft au niveau de ses serveurs.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-windows-autopatch-bug-installing-restricted-drivers/){:target="_blank"}
