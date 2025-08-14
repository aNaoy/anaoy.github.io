---
title: 'Microsoft fixes Windows Server bug causing cluster, VM issues'
date: 2025-08-14
permalink: /posts/2025/08/14/microsoft-fixes-windows-server-bug-causing-cluster-vm-issues/
tags:
- veille-cyber
- bleepingcomp
---
**Correction d'un bug affectant les clusters Windows Server**

Une mise à jour de sécurité Windows Server de juillet avait causé des problèmes de fonctionnement du service de cluster, entraînant des redémarrages de nœuds et de machines virtuelles. Ce dysfonctionnement pouvait également provoquer des erreurs sur les systèmes utilisant le chiffrement BitLocker sur les volumes partagés de cluster (CSV). Microsoft a identifié cette vulnérabilité comme un problème connu.

**Points clés :**

*   La mise à jour KB5062557 de juillet pour Windows Server 2019 était à l'origine du problème.
*   Les symptômes incluaient l'arrêt et le redémarrage répétés du service de cluster, des échecs de réintégration des nœuds dans le cluster, des quarantaines, des redémarrages multiples de VM et des erreurs Event ID 7031.
*   Les systèmes utilisant BitLocker sur les CSV étaient particulièrement affectés.

**Vulnérabilités :**

*   Aucun numéro CVE spécifique n'est mentionné dans l'article pour ce problème particulier.

**Recommandations :**

*   Installer la mise à jour cumulative d'août 2025, KB5063877, pour Windows Server 2019.
*   Avant d'installer KB5063877, il est nécessaire de déployer la mise à jour de la pile de maintenance KB5005112.
*   Ces mises à jour peuvent être obtenues via Windows Update, le catalogue Microsoft Update, ou Windows Server Update Services (WSUS).
*   En cas de difficultés, il était conseillé de contacter le support technique de Microsoft pour les entreprises.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-windows-server-bug-causing-cluster-vm-issues/){:target="_blank"}
