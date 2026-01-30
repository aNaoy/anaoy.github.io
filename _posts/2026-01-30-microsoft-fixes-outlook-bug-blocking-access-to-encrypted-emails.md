---
title: 'Microsoft fixes Outlook bug blocking access to encrypted emails'
date: 2026-01-30
permalink: /posts/2026/01/30/microsoft-fixes-outlook-bug-blocking-access-to-encrypted-emails/
tags:
- veille-cyber
- bleepingcomp
---
**Correction d'un bug dans Outlook affectant les e-mails chiffrés**

Microsoft a résolu un problème qui empêchait les utilisateurs de Microsoft 365 d'ouvrir des e-mails chiffrés dans la version classique d'Outlook. Ce bogue, introduit lors d'une mise à jour de décembre, se manifestait par un fichier `message_v2.rpmsg` au lieu du contenu lisible, rendant les messages chiffrés inaccessibles.

Le problème concernait spécifiquement les e-mails marqués avec les permissions "Chiffrer uniquement" (Encrypt Only), une politique qui n'empêche pas le transfert, l'impression ou la copie du message. Lors de la tentative d'ouverture, un message indiquait que l'élément ne pouvait pas être vu dans le volet de lecture sans vérification des identifiants.

**Points clés :**
*   **Problème :** Incapacité d'ouvrir des e-mails chiffrés avec "Chiffrer uniquement" dans la version classique d'Outlook.
*   **Cause :** Un bug introduit par une mise à jour de décembre.
*   **Symptôme :** Affichage d'un fichier `message_v2.rpmsg` au lieu du contenu de l'e-mail.
*   **Impact :** Rend les e-mails chiffrés inaccessibles.

**Vulnérabilités :**
Aucun identifiant CVE spécifique n'est mentionné dans l'article pour ce bug.

**Recommandations :**
*   **Mise à jour :** Microsoft a déployé un correctif pour les canaux Beta, avec un déploiement prévu pour les canaux Current et Current Preview en février. Il est conseillé de mettre à jour Outlook vers une version corrigée dès que possible.
*   **Solutions de contournement temporaires :**
    *   **Pour les expéditeurs :** Utiliser l'option "Chiffrer" sous le ruban "Options" au lieu de la boîte de dialogue "Fichier".
    *   **Pour les utilisateurs :** Revenir à une version antérieure non affectée d'Outlook en exécutant la commande suivante depuis une invite de commande élevée :
        `"%programfiles%\Common Files\Microsoft Shared\ClickToRun\officec2rclient.exe" /update user updatetoversion=16.0.19426.20186`

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-outlook-bug-blocking-access-to-encrypted-emails/){:target="_blank"}
