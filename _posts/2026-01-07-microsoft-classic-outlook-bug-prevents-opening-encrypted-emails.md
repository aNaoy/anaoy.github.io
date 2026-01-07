---
title: 'Microsoft: Classic Outlook bug prevents opening encrypted emails'
date: 2026-01-07
permalink: /posts/2026/01/07/microsoft-classic-outlook-bug-prevents-opening-encrypted-emails/
tags:
- veille-cyber
- bleepingcomp
---
### Blocage d'ouverture d'emails chiffrés dans Outlook

Une mise à jour récente du client de messagerie Outlook classique (Version 2511, Build 19426.20218) a introduit un problème empêchant les utilisateurs d'ouvrir les emails chiffrés avec la permission "Chiffrer uniquement". Ces messages, qui autorisent normalement la copie, l'impression et le transfert, s'affichent comme une pièce jointe nommée `message_v2.rpmsg` au lieu de leur contenu lisible. Le message d'erreur indique : "Ce message avec des autorisations restreintes ne peut pas être lu dans le volet de lecture tant que vous n'avez pas vérifié vos informations d'identification. Ouvrez l'élément pour lire son contenu et vérifier vos informations d'identification."

**Points clés :**

*   Le problème concerne le client Outlook classique.
*   Il affecte spécifiquement les emails chiffrés avec la permission "Chiffrer uniquement".
*   Une mise à jour de version est identifiée comme la cause.

**Vulnérabilités :**

*   Aucun identifiant CVE n'est mentionné dans l'article pour ce bug spécifique.

**Recommandations et solutions :**

*   **Solution de contournement pour les expéditeurs :** Enregistrer l'email après l'avoir chiffré et avant de l'envoyer.
*   **Solution de contournement pour les destinataires :** Revenir à une version antérieure d'Outlook. Pour ce faire, fermez toutes les applications Office et exécutez la commande suivante depuis une invite de commande élevée :
    `"%programfiles%\Common Files\Microsoft Shared\ClickToRun\officec2rclient.exe" /update user updatetoversion=16.0.19426.20186`
*   Microsoft enquête sur le problème et travaille à un correctif permanent, mais aucun calendrier de résolution n'a été communiqué.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-classic-outlook-bug-prevents-opening-encrypted-emails/){:target="_blank"}
