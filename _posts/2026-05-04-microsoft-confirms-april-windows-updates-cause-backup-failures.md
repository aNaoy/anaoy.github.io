---
title: 'Microsoft confirms April Windows updates cause backup failures'
date: 2026-05-04
permalink: /posts/2026/05/04/microsoft-confirms-april-windows-updates-cause-backup-failures/
tags:
- veille-cyber
- bleepingcomp
---
### Impact des mises à jour Windows d'avril sur les logiciels de sauvegarde

Les mises à jour de sécurité de Windows d'avril 2026 provoquent des dysfonctionnements dans de nombreuses applications de sauvegarde tierces. Ce problème survient suite à l'ajout du pilote `psmounterex.sys` à la liste de blocage des pilotes vulnérables de Microsoft, entraînant des erreurs de timeout lors de l'utilisation du service VSS (Volume Shadow Copy Service).

**Points clés :**
*   Le blocage est intentionnel : Microsoft a renforcé la sécurité pour contrer l'exploitation d'une faille critique.
*   Les logiciels touchés incluent, entre autres, Macrium Reflect, Acronis Cyber Protect Cloud, UrBackup et NinjaOne.
*   Le blocage empêche le montage d'images de sauvegarde, bien que la création de sauvegardes puisse parfois aboutir.
*   Les utilisateurs peuvent vérifier si le pilote est bloqué en consultant l'**événement 3077** dans l'Observateur d'événements (Code Integrity Operational log).

**Vulnérabilité corrigée :**
*   **CVE-2023-43896** : Une vulnérabilité de type dépassement de tampon (buffer overflow) dans le pilote `psmounterex.sys`, permettant une élévation de privilèges ou l'exécution de code arbitraire.

**Recommandations :**
*   **Ne pas désinstaller ni suspendre les mises à jour Windows**, car celles-ci sont nécessaires pour protéger le système contre la CVE-2023-43896.
*   **Mettre à jour les applications de sauvegarde** : Installez la version la plus récente de votre logiciel de sauvegarde, car les éditeurs intègrent désormais des pilotes corrigés compatibles avec les nouvelles règles de sécurité de Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-confirms-backup-failures-caused-by-vulnerable-driver-block/){:target="_blank"}
