---
title: 'Mail2Shell zero-click attack lets hackers hijack FreeScout mail servers'
date: 2026-03-04
permalink: /posts/2026/03/04/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Attaque Mail2Shell : Contrôle total des serveurs FreeScout par email**

Une faille de sécurité critique, identifiée sous le nom de **CVE-2026-28289**, permet une exécution de code à distance sans interaction utilisateur ni authentification sur la plateforme d'aide FreeScout. Cette vulnérabilité contourne une correction précédente (CVE-2026-27636) destinée aux utilisateurs authentifiés avec des permissions d'upload.

Des chercheurs ont découvert qu'un attaquant peut exploiter cette faille en envoyant un simple email malveillant à une adresse configurée dans FreeScout. L'utilisation d'un caractère d'espace sans largeur (Unicode U+200B) permet de contourner les nouvelles protections mises en place pour les noms de fichiers, faisant croire que le fichier est un fichier caché (dotfile) et déclenchant ainsi la vulnérabilité.

Une fois le fichier malveillant (comme un `.htaccess`) téléchargé et stocké, l'attaquant peut y accéder via l'interface web et exécuter des commandes sur le serveur, le tout sans avoir besoin de s'authentifier.

**Points Clés :**

*   **Type de vulnérabilité :** Exécution de code à distance (RCE) "zero-click".
*   **Impact :** Compromission totale du serveur, fuites de données, mouvement latéral dans les réseaux internes et interruption de service.
*   **Cible :** La plateforme d'aide et de messagerie partagée FreeScout, une alternative auto-hébergée à Zendesk ou Help Scout.
*   **Diffusion :** L'attaque est déclenchée par l'envoi d'un email contenant une pièce jointe spécialement conçue.

**Vulnérabilités :**

*   **CVE-2026-28289 :** Vulnérabilité critique permettant le contournement des protections et l'exécution de code à distance sans interaction.
*   **CVE-2026-27636 :** Vulnérabilité précédente contournée par CVE-2026-28289, qui pouvait être exploitée par des utilisateurs authentifiés avec des permissions d'upload.

**Recommandations :**

*   **Mise à jour immédiate :** Mettre à jour FreeScout vers la version 1.8.207 ou supérieure. Les versions antérieures à 1.8.207 sont affectées.
*   **Configuration Apache :** Désactiver l'option `AllowOverrideAll` dans la configuration d'Apache, même après la mise à jour vers la version 1.8.207.

Bien qu'aucune exploitation active n'ait été observée pour le moment, le risque d'attaques futures est jugé élevé en raison de la gravité de la faille.

---
[Source](https://www.bleepingcomputer.com/news/security/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/){:target="_blank"}
