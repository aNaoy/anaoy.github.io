---
title: 'iCloud Calendar abused to send phishing emails from Apple’s servers'
date: 2025-09-07
permalink: /posts/2025/09/07/icloud-calendar-abused-to-send-phishing-emails-from-apples-servers/
tags:
- veille-cyber
- bleepingcomp
---
**Escroqueries par Calendrier iCloud : Appels Piégés et Courriels Indésirables**

Une nouvelle technique d'hameçonnage est exploitée en utilisant les invitations de calendrier iCloud pour envoyer des courriels se faisant passer pour des notifications d'achat Apple. Ces messages, envoyés depuis les serveurs de messagerie légitimes d'Apple (`noreply@email.apple.com`), sont conçus pour contourner les filtres anti-spam et inciter les destinataires à appeler un numéro de téléphone frauduleux.

Les courriels prétendent être des reçus de paiement pour des achats non autorisés (par exemple, 599 $ sur PayPal) et fournissent un numéro de contact pour "résoudre" le problème. Au téléphone, les escrocs tentent de convaincre la victime que son compte est compromis et l'incitent à télécharger et exécuter un logiciel, ouvrant la porte au vol d'argent, au déploiement de logiciels malveillants ou à l'exfiltration de données.

Cette méthode exploite la fonction d'invitation de calendrier d'iCloud, où le contenu de l'escroquerie est placé dans le champ des notes de l'événement. Les invitations sont envoyées à des adresses e-mail Microsoft 365 qui semblent faire partie d'une liste de diffusion, permettant ainsi de toucher un grand nombre de cibles. Le mécanisme de réécriture d'expéditeur (SRS) de Microsoft 365 est utilisé pour que ces courriels, bien qu'originaires d'Apple, puissent passer les contrôles d'authentification lors de leur transfert.

**Points Clés :**

*   Utilisation abusive des invitations de calendrier iCloud pour envoyer des courriels de phishing.
*   Les courriels proviennent des serveurs légitimes d'Apple (`noreply@email.apple.com`), renforçant leur crédibilité.
*   Les escroqueries sont déguisées en notifications d'achat non sollicitées, incitant à l'appel d'un faux support technique.
*   L'objectif est d'amener la victime à installer des logiciels malveillants ou à divulguer des informations sensibles.

**Vulnérabilités (Non spécifiées avec CVE dans l'article) :**

*   L'abus de la fonctionnalité d'envoi d'invitations de calendrier iCloud.
*   La confiance accordée aux courriels provenant des serveurs d'Apple.

**Recommandations :**

*   Soyez extrêmement prudent face aux invitations de calendrier inattendues, surtout si elles contiennent des messages étranges ou des demandes d'action urgente.
*   Ne contactez jamais les numéros de téléphone fournis dans des courriels suspects se faisant passer pour des entreprises. Recherchez les canaux de contact officiels des services que vous utilisez.
*   Ne téléchargez ni n'exécutez jamais de logiciels à la demande d'une personne non sollicitée par téléphone ou par e-mail.
*   Vérifiez toujours l'authenticité des notifications de paiement ou de compte via les applications ou sites web officiels des services concernés.

---
[Source](https://www.bleepingcomputer.com/news/security/icloud-calendar-abused-to-send-phishing-emails-from-apples-servers/){:target="_blank"}
