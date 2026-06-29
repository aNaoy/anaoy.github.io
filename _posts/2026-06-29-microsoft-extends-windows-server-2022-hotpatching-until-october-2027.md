---
title: 'Microsoft extends Windows Server 2022 hotpatching until October 2027'
date: 2026-06-29
permalink: /posts/2026/06/29/microsoft-extends-windows-server-2022-hotpatching-until-october-2027/
tags:
- veille-cyber
- bleepingcomp
---
### Prolongation du support Hotpatch pour Windows Server 2022

Microsoft a prolongé la disponibilité du support « Hotpatch » pour Windows Server 2022 jusqu'en octobre 2027, soit un an après la fin du support standard prévue en octobre 2026. Cette technologie permet d'appliquer les mises à jour de sécurité directement sur les processus en cours d'exécution, éliminant ainsi le besoin de redémarrer le système après chaque déploiement.

**Points clés :**
*   **Éligibilité :** Cette extension concerne exclusivement les systèmes sous **Windows Server 2022 Datacenter: Azure Edition**.
*   **Fonctionnement :** Les mises à jour de sécurité sont injectées en mémoire, réduisant les interruptions de service et le temps d'exposition aux vulnérabilités.
*   **Limites :** Le redémarrage reste obligatoire pour les mises à jour non liées à la sécurité (ex: correctifs .NET) ou pour les mises à jour classiques non déployées via le canal Hotpatch.
*   **Évolutions :** La technologie Hotpatch est en cours de généralisation sur Windows Server 2025, Windows 11 24H2 et Windows 365. À partir de mai 2026, elle sera activée par défaut pour les appareils éligibles gérés via Intune et Microsoft Graph API.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, mais le Hotpatch est une mesure proactive visant à réduire la fenêtre d'exposition aux vulnérabilités en permettant une application immédiate des correctifs sans contrainte de maintenance.

**Recommandations :**
*   Pour les organisations utilisant Windows Server 2022, migrer ou privilégier l'édition **Datacenter: Azure Edition** pour bénéficier de cette fonctionnalité de patching sans redémarrage.
*   Anticiper l'activation par défaut du Hotpatch sur les parcs Windows gérés par Intune dès mai 2026 pour optimiser la réactivité face aux menaces.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-extends-windows-server-2022-hotpatching-until-october-2027/){:target="_blank"}
