---
title: 'Microsoft fixes bug that removed Copilot buttons in Outlook'
date: 2026-07-02
permalink: /posts/2026/07/02/microsoft-fixes-bug-that-removed-copilot-buttons-in-outlook/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution des anomalies d'affichage de Copilot dans Outlook

Microsoft a corrigé un problème technique affectant les utilisateurs de la version classique d'Outlook sur Windows, provoquant la disparition inopinée des boutons et fonctionnalités de Copilot pour les détenteurs de licences « Copilot Chat (Basic) ».

**Points clés :**
*   Le dysfonctionnement se manifestait par l'absence du bouton Copilot dans le ruban supérieur et la barre de navigation latérale.
*   Certaines fonctionnalités restaient accessibles, mais inopérantes, ou apparaissaient comme grisées.
*   Le problème était limité à l'application Outlook classique ; l'accès via Outlook Web ou l'application autonome Microsoft 365 Copilot restait fonctionnel.
*   Une instabilité distincte est actuellement à l'étude concernant des plantages d'Outlook sur les systèmes utilisant l'antivirus Kaspersky (module `mcou.dll`).

**Vulnérabilités :**
*   Aucun identifiant CVE n'est associé à ces incidents de fonctionnement. Il s'agit de bugs logiciels internes et de conflits de compatibilité logicielle.

**Recommandations :**
*   **Pour le bug d'affichage de Copilot :** Redémarrer l'application Outlook pour appliquer la modification de service déployée le 29 juin 2026. Si le problème persiste, mettre à jour le client via *Fichier > Compte Office > Options de mise à jour > Mettre à jour maintenant*. En cas d'échec, basculer sur la version web ou utiliser la nouvelle interface d'Outlook.
*   **Pour les plantages liés à Kaspersky :** Vérifier les journaux d'événements Windows pour identifier l'« Événement 1000 » impliquant `MCOU.DLL`. En cas de confirmation, contacter le support technique de Kaspersky pour une assistance dédiée.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-bug-that-removed-copilot-button-in-outlook/){:target="_blank"}
