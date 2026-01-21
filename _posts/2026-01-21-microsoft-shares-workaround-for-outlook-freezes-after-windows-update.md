---
title: 'Microsoft shares workaround for Outlook freezes after Windows update'
date: 2026-01-21
permalink: /posts/2026/01/21/microsoft-shares-workaround-for-outlook-freezes-after-windows-update/
tags:
- veille-cyber
- bleepingcomp
---
### Problèmes avec Outlook suite à une mise à jour Windows

Une mise à jour de sécurité récente de Windows, spécifiquement KB5074109, cause des blocages sur l'application de bureau classique Outlook, particulièrement pour les utilisateurs de comptes e-mail POP. Ce problème affecte les versions Windows 11 25H2 et 24H2, ainsi que plusieurs versions de Windows 10 et Windows Server (2025, 2022, 2019).

Les symptômes observés incluent :
*   Blocage de l'application Outlook, nécessitant une fermeture forcée via le Gestionnaire des tâches ou un redémarrage du système.
*   Relocalisation des e-mails déjà téléchargés.
*   Non-apparition des e-mails envoyés dans le dossier "Éléments envoyés".
*   Dans certains cas, toute application pourrait devenir instable ou rencontrer des erreurs inattendues lors de l'ouverture ou de l'enregistrement de fichiers depuis des stockages cloud comme OneDrive ou Dropbox, notamment lorsque les fichiers PST d'Outlook sont stockés sur OneDrive.

Microsoft enquête sur ces problèmes et propose des solutions temporaires en attendant un correctif définitif.

**Points clés :**

*   La mise à jour KB5074109 de Windows cause des instabilités avec Outlook.
*   Les utilisateurs de comptes POP et de stockages cloud comme OneDrive sont particulièrement touchés.
*   Des symptômes variés sont rapportés, allant des blocages de l'application aux problèmes de synchronisation des e-mails.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques liées directement à ces problèmes d'Outlook. Il est plutôt question de bugs logiciels introduits par une mise à jour.

**Recommandations :**

*   **Solution de contournement immédiate :** Accéder à sa messagerie via l'interface webmail.
*   **Solution de contournement pour les fichiers PST :** Déplacer les fichiers PST d'Outlook hors de OneDrive.
*   **Désinstallation de la mise à jour :** Il est possible de désinstaller les mises à jour KB5074109 ou KB5073724 via les paramètres Windows. Cependant, Microsoft déconseille fortement cette pratique, car la suppression des mises à jour de sécurité peut exposer le système à des malwares et autres menaces.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-shares-workaround-for-outlook-freezes-after-windows-update/){:target="_blank"}
