---
title: 'Mail2Shell zero-click attack lets hackers hijack FreeScout mail servers'
date: 2026-03-05
permalink: /posts/2026/03/05/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Attaque Mail2Shell : Prise de contrôle des serveurs FreeScout**

Une faille critique, identifiée comme CVE-2026-28289, permet une exécution de code à distance (RCE) sur la plateforme d'assistance FreeScout sans aucune interaction utilisateur ni authentification. Cette vulnérabilité contourne une correction précédente (CVE-2026-27636) qui affectait les utilisateurs authentifiés ayant des permissions d'upload.

**Points Clés :**

*   **Nature de l'attaque :** "Zero-click" et à distance.
*   **Mode d'exploitation :** L'envoi d'un unique email spécialement conçu à une adresse configurée dans FreeScout suffit à déclencher l'exploitation.
*   **Mécanisme de contournement :** L'utilisation d'un caractère d'espace sans chasse (Unicode U+200B) avant le nom d'un fichier joint permet de contourner les mécanismes de validation des noms de fichiers (comme les extensions restreintes ou les noms commençant par un point). Après le traitement, ce caractère disparaît, permettant la sauvegarde du fichier comme un "dotfile", activant ainsi l'exploitation de CVE-2026-27636.
*   **Impact :** L'attaquant peut accéder au fichier malveillant téléchargé via l'interface web et exécuter des commandes sur le serveur. Les conséquences potentielles incluent la compromission totale du serveur, des fuites de données, des mouvements latéraux dans les réseaux internes et des interruptions de service.

**Vulnérabilités :**

*   **CVE-2026-28289 :** Vulnérabilité de contournement de correctif permettant une RCE sans interaction ni authentification.
*   **CVE-2026-27636 :** Vulnérabilité RCE antérieure, exploitable par des utilisateurs authentifiés avec des permissions d'upload.

**Recommandations :**

*   **Mise à jour immédiate :** Appliquer le correctif disponible dans FreeScout version 1.8.207 ou ultérieure. Les versions jusqu'à 1.8.206 sont affectées.
*   **Configuration Apache :** Désactiver l'option ‘AllowOverrideAll’ dans la configuration Apache du serveur FreeScout, même après la mise à jour.

Bien qu'aucune exploitation active de CVE-2026-28289 n'ait été observée publiquement au moment de la publication, le risque d'attaques futures est jugé très élevé.

---
[Source](https://www.bleepingcomputer.com/news/security/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/){:target="_blank"}
