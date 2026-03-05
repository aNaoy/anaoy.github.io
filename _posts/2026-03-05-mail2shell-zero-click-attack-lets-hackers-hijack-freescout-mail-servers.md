---
title: 'Mail2Shell zero-click attack lets hackers hijack FreeScout mail servers'
date: 2026-03-05
permalink: /posts/2026/03/05/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/
tags:
- veille-cyber
- bleepingcomp
---
## Attaque "Mail2Shell" : Exécution de code à distance sur les serveurs FreeScout

Une faille critique dans la plateforme de helpdesk FreeScout permet aux attaquants d'exécuter du code à distance sur les serveurs sans aucune interaction ni authentification utilisateur. Cette vulnérabilité, référencée sous le code **CVE-2026-28289**, contourne une correction précédente visant à empêcher l'exécution de code à distance par des utilisateurs authentifiés disposant de permissions de téléchargement.

L'exploitation consiste à envoyer un seul e-mail malveillant contenant une pièce jointe à une adresse configurée dans FreeScout. L'attaquant peut alors accéder au fichier joint, qui est stocké sur le serveur, via l'interface web. Le caractère clé de cette attaque réside dans l'utilisation d'un espace sans chasse (Unicode U+200B) avant le nom du fichier. Ce caractère, invisible, permet de contourner le mécanisme de validation qui visait à bloquer les fichiers avec des extensions restreintes ou commençant par un point. Après traitement, le caractère invisible est supprimé, permettant au fichier d'être sauvegardé en tant que "dotfile" et déclenchant ainsi l'exécution du code malveillant.

Cette vulnérabilité affecte toutes les versions de FreeScout jusqu'à la version 1.8.206 incluse. Une version corrigée, la 1.8.207, a été publiée.

**Points Clés :**

*   **Type de vulnérabilité :** Exécution de code à distance (RCE) sans interaction utilisateur (zero-click).
*   **Cible :** Plateforme de helpdesk FreeScout.
*   **Mécanisme d'exploitation :** Envoi d'un e-mail avec une pièce jointe malveillante contenant un espace sans chasse avant le nom du fichier.
*   **Impact :** Compromission totale du serveur, fuites de données, mouvements latéraux sur le réseau interne et interruptions de service.

**Vulnérabilités :**

*   **CVE-2026-28289 :** Faille critique permettant l'exécution de code à distance sans interaction ni authentification.
*   **CVE-2026-27636 :** Vulnérabilité antérieure d'exécution de code à distance, que CVE-2026-28289 permet de contourner.

**Recommandations :**

*   **Mise à jour immédiate :** Les utilisateurs de FreeScout doivent impérativement passer à la version 1.8.207 ou une version ultérieure.
*   **Configuration Apache :** Il est recommandé de désactiver l'option `AllowOverrideAll` dans la configuration Apache du serveur FreeScout, même après la mise à jour.

Bien qu'aucune exploitation active n'ait été détectée à ce jour, le risque est jugé élevé compte tenu de la nature de cette faille.

---
[Source](https://www.bleepingcomputer.com/news/security/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/){:target="_blank"}
