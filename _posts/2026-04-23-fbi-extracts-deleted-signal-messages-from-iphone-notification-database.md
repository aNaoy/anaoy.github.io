---
title: 'FBI Extracts Deleted Signal Messages from iPhone Notification Database'
date: 2026-04-23
permalink: /posts/2026/04/23/fbi-extracts-deleted-signal-messages-from-iphone-notification-database/
tags:
- veille-cyber
- schneier
---
### Failles dans la confidentialité de Signal sur iPhone : l'accès du FBI aux notifications

Le FBI a réussi à récupérer des messages Signal supprimés sur un iPhone saisi en exploitant la base de données des notifications push du système iOS. Bien que les messages aient été effacés de l'application elle-même, le système d'exploitation avait conservé des copies du contenu dans sa mémoire interne, là où les aperçus de notifications sont stockés.

**Points clés :**
*   **Vulnérabilité de conception :** La persistance des données ne réside pas dans l'application Signal, mais dans la manière dont iOS gère et stocke les journaux de notifications.
*   **Risque judiciaire :** L'extraction forensique par les autorités permet de contourner le chiffrement de l'application en accédant aux données résiduelles conservées par le système.
*   **Absence de CVE :** Ce problème relève d'une vulnérabilité comportementale liée à l'architecture d'iOS et aux paramètres utilisateur plutôt qu'à une faille logicielle spécifique (CVE) corrigeable par un correctif.

**Recommandations :**
*   **Désactiver les aperçus :** Configurer Signal pour masquer le contenu des messages dans les notifications (paramètre « Afficher » réglé sur « Nom uniquement » ou « Aucun »).
*   **Sécurisation iOS :** Dans les réglages de confidentialité d'Apple, désactiver les aperçus des notifications sur l'écran de verrouillage pour limiter la trace des données sensibles en mémoire.
*   **Conscience du risque :** Comprendre que les messages chiffrés de bout en bout ne garantissent pas la confidentialité si le système d'exploitation enregistre des copies en clair dans ses journaux système.

---
[Source](https://www.schneier.com/blog/archives/2026/04/fbi-extracts-deleted-signal-messages-from-iphone-notification-database.html){:target="_blank"}
