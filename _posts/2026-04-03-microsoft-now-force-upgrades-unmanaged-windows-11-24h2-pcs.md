---
title: 'Microsoft now force upgrades unmanaged Windows 11 24H2 PCs'
date: 2026-04-03
permalink: /posts/2026/04/03/microsoft-now-force-upgrades-unmanaged-windows-11-24h2-pcs/
tags:
- veille-cyber
- bleepingcomp
---
### Migration forcée vers Windows 11 25H2

Microsoft a initié le déploiement automatique de la mise à jour Windows 11 25H2 pour les appareils grand public (éditions Home et Pro) non gérés par des services informatiques. Cette mesure vise à garantir que les systèmes continuent de recevoir les correctifs de sécurité critiques, le support technique et les mises à jour de fuseaux horaires. Bien que la version 24H2 soit officiellement supportée jusqu'au 13 octobre 2026, cette automatisation assure une transition préventive vers la version la plus récente.

**Points clés :**
*   **Automatisation :** La mise à jour s'installe via des packages d'activation légers (moins de 200 Ko).
*   **Flexibilité :** Les utilisateurs peuvent différer le redémarrage ou suspendre temporairement les mises à jour via les paramètres Windows, bien que l'installation reste obligatoire à terme.
*   **Contexte sécuritaire :** Microsoft a récemment publié des correctifs d'urgence pour divers problèmes, incluant des erreurs de connexion aux comptes Microsoft et des vulnérabilités critiques dans le service RRAS (Routing and Remote Access Service).

**Vulnérabilités :**
*   L'article mentionne une faille RCE (exécution de code à distance) dans l'outil de gestion RRAS, corrigée via des mises à jour hors bande (OOB) pour les appareils sous Windows 11 Entreprise. *Note : Aucun identifiant CVE spécifique n'a été fourni dans le texte source pour cette vulnérabilité.*

**Recommandations :**
*   **Vérification manuelle :** Si la mise à jour automatique n'a pas encore eu lieu, il est possible de forcer son installation via *Paramètres > Windows Update*.
*   **Gestion des erreurs :** En cas d'échec lors du processus d'installation, consulter le [guide de dépannage officiel de Microsoft](https://support.microsoft.com/en-us/help/10164/fix-windows-update-errors).
*   **Mise à jour système :** Maintenir les systèmes à jour est indispensable pour bénéficier des protections contre les menaces de sécurité récentes et éviter l'interruption du support technique.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-now-force-upgrades-unmanaged-windows-11-24h2-pcs/){:target="_blank"}
