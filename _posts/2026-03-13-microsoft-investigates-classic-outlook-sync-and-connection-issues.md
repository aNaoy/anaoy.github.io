---
title: 'Microsoft investigates classic Outlook sync and connection issues'
date: 2026-03-13
permalink: /posts/2026/03/13/microsoft-investigates-classic-outlook-sync-and-connection-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Problèmes de synchronisation et de stabilité dans Outlook Classic

Microsoft enquête actuellement sur plusieurs dysfonctionnements affectant le client de bureau Outlook "Classic" :

**Points clés :**
*   **Erreurs de création de groupes :** Les utilisateurs rencontrent des erreurs "Can't connect to the server" lors de la création de groupes Exchange, dues à une défaillance de l'appel AD Graph.
*   **Problèmes de synchronisation Gmail/Yahoo :** Des erreurs (codes 0x800CCC0F et 0x80070057) surviennent après un changement de mot de passe, le client ne sollicitant plus l'authentification.
*   **Bug d'interface :** Un problème persistant provoque la disparition du curseur de la souris dans Outlook, OneNote et d'autres applications Microsoft 365.

**Vulnérabilités :**
*   Aucun identifiant CVE n'est associé à ces incidents, il s'agit de bugs fonctionnels et non de failles de sécurité exploitables.

**Recommandations :**
*   **Pour les groupes :** Utiliser la version "New Outlook" ou Outlook Web Access (OWA) pour gérer les groupes en attendant une mise à jour utilisant l'API REST.
*   **Pour les comptes Gmail/Yahoo :** Supprimer manuellement les entrées de registre correspondantes dans `Computer\HKEY_CURRENT_USER\Software\Microsoft\Office.0\Common\Identity\Identities`.
*   **Pour le curseur disparu :** Tenter de cliquer sur un message ou basculer sur PowerPoint pour restaurer le pointeur ; en dernier recours, redémarrer le poste de travail. En cas de persistance, il est conseillé d'ouvrir un ticket de support via l'interface d'administration Microsoft 365.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-investigates-classic-outlook-sync-and-connection-issues/){:target="_blank"}
