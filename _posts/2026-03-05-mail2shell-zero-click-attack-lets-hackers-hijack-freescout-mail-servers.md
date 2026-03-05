---
title: 'Mail2Shell zero-click attack lets hackers hijack FreeScout mail servers'
date: 2026-03-05
permalink: /posts/2026/03/05/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/
tags:
- veille-cyber
- bleepingcomp
---
## Risque Critique : Exécution de Code à Distance sur FreeScout

Une vulnérabilité de sévérité maximale, identifiée sous **CVE-2026-28289**, a été découverte dans la plateforme d'assistance FreeScout. Celle-ci permet une exécution de code à distance (RCE) sans aucune interaction utilisateur ni authentification.

Cette faille contourne une précédente correction (CVE-2026-27636) qui nécessitait des permissions de téléchargement et une authentification pour être exploitée.

### Points Clés :

*   **Attaque "zero-click"** : Les attaquants peuvent exploiter cette vulnérabilité en envoyant un seul e-mail spécialement conçu à une adresse configurée dans FreeScout.
*   **Contournement des sécurités** : Un caractère d'espace sans largeur (Unicode U+200B) inséré avant le nom d'un fichier d'attachement permet de contourner le mécanisme de validation des noms de fichiers. Ce caractère, non visible, est supprimé lors du traitement, permettant au fichier d'être enregistré comme un "dotfile" (.htaccess), déclenchant ainsi l'exploitation de la vulnérabilité précédente.
*   **Impact potentiel** : L'exploitation réussie de CVE-2026-28289 peut entraîner une compromission totale du serveur, des fuites de données, des déplacements latéraux sur les réseaux internes et des interruptions de service.

### Vulnérabilités :

*   **CVE-2026-28289** : Permet l'exécution de code à distance (RCE) via l'envoi d'un e-mail contenant un fichier d'attachement malveillant.
*   **CVE-2026-27636** : Vulnérabilité RCE précédente, exploitée ici via le contournement du mécanisme de validation des fichiers.

### Recommandations :

*   **Mise à jour immédiate** : Il est impératif de mettre à jour FreeScout vers la version **1.8.207** ou supérieure, qui corrige cette faille.
*   **Configuration Apache** : Il est également recommandé de désactiver l'option `AllowOverrideAll` dans la configuration Apache du serveur FreeScout, même après la mise à jour vers la version 1.8.207.

Bien qu'aucune exploitation active n'ait été observée pour l'instant, le risque est jugé très élevé en raison de la nature de la faille.

---
[Source](https://www.bleepingcomputer.com/news/security/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/){:target="_blank"}
