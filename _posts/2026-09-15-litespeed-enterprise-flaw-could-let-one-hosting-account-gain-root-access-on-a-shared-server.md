---
title: 'LiteSpeed Enterprise Flaw Could Let One Hosting Account Gain Root Access on a Shared Server'
date: 2026-09-15
permalink: /posts/2026/09/15/litespeed-enterprise-flaw-could-let-one-hosting-account-gain-root-access-on-a-shared-server/
tags:
- veille-cyber
- hackernews
---
### Risque d'élévation de privilèges critique dans LiteSpeed Web Server Enterprise

Une vulnérabilité critique a été identifiée dans **LiteSpeed Web Server Enterprise** (versions antérieures à 6.3.7), permettant à un utilisateur disposant d'un accès restreint sur un serveur mutualisé d'obtenir les privilèges « root ».

**Points clés :**
* **Impact majeur :** L'exploitation permet de contourner les mécanismes d'isolation des comptes (y compris **CageFS**), offrant un accès total aux fichiers, aux autres sites hébergés sur la machine et à la configuration du serveur.
* **Absence d'identifiant :** À ce jour, aucune CVE n'a été attribuée et aucun score de criticité n'a été publié.
* **Contexte :** Il s'agit de la troisième vulnérabilité liée à l'écosystème LiteSpeed sur cPanel signalée cette année permettant une escalade vers le compte root, bien qu'il s'agisse de la première affectant directement le serveur web lui-même.
* **État des mises à jour :** Les mises à jour automatiques peuvent être différées, rendant une intervention manuelle nécessaire.

**Vulnérabilités :**
* **CVE :** Aucune assignée à ce jour.
* **Version affectée :** < 6.3.7.

**Recommandations :**
* **Mise à jour immédiate :** Les administrateurs doivent mettre à jour manuellement vers la version **6.3.7** en exécutant la commande suivante :
  `/usr/local/lsws/admin/misc/lsup.sh -f -v 6.3.7`
* **Restauration des mises à jour automatiques :** Après la mise à jour manuelle, il est conseillé de réactiver le suivi du canal stable via la commande :
  `touch /usr/local/lsws/autoupdate/follow_stable`
* **Vigilance :** Surveiller les journaux du système, bien qu'aucun indicateur de compromission spécifique n'ait été fourni par l'éditeur.

---
[Source](https://thehackernews.com/2026/09/litespeed-enterprise-flaw-could-let-one.html){:target="_blank"}
