---
title: 'Mail2Shell zero-click attack lets hackers hijack FreeScout mail servers'
date: 2026-03-05
permalink: /posts/2026/03/05/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Détournement de serveurs FreeScout via une vulnérabilité de type "zero-click"**

Une faille critique, identifiée sous la référence CVE-2026-28289, permet à des attaquants d'exécuter du code à distance sur les serveurs de messagerie utilisant la plateforme d'assistance FreeScout, sans aucune interaction utilisateur ni authentification.

Cette vulnérabilité contourne une correction précédente (CVE-2026-27636) qui nécessitait une authentification et des permissions de téléchargement. L'exploitation repose sur l'envoi d'un e-mail spécialement conçu contenant une pièce jointe malveillante. Grâce à l'utilisation d'un caractère invisible (espace de largeur nulle, Unicode U+200B) avant le nom du fichier, les mécanismes de validation sont déjoués, permettant au fichier d'être enregistré comme un fichier de configuration (.htaccess dans certains cas) qui déclenche ensuite l'exécution de code. La pièce jointe est stockée dans un répertoire accessible via l'interface web, rendant l'attaque effective sans aucune action de la part d'un utilisateur.

**Points clés :**

*   **Nature de l'attaque :** "Zero-click" RCE (Remote Code Execution).
*   **Mécanisme :** Contournement des validations de fichiers à l'aide d'un caractère invisible.
*   **Impact potentiel :** Prise de contrôle complète du serveur, fuites de données, mouvement latéral sur le réseau, interruption de service.
*   **Contexte :** FreeScout est une plateforme d'assistance open-source largement utilisée.

**Vulnérabilités :**

*   **CVE-2026-28289 :** Permet l'exécution de code à distance sans authentification via un e-mail piégé.
*   **CVE-2026-27636 :** Vulnérabilité précédente sur l'exécution de code à distance, qui est contournée par la nouvelle faille.

**Recommandations :**

*   **Mise à jour immédiate :** Appliquer la version 1.8.207 ou ultérieure de FreeScout.
*   **Configuration Apache :** Désactiver 'AllowOverrideAll' dans la configuration Apache, même après la mise à jour.

Bien qu'aucune exploitation active n'ait été signalée, le risque est jugé élevé étant donné la simplicité de déclenchement de la faille.

---
[Source](https://www.bleepingcomputer.com/news/security/mail2shell-zero-click-attack-lets-hackers-hijack-freescout-mail-servers/){:target="_blank"}
