---
title: 'Apple account change alerts abused to send phishing emails'
date: 2026-04-19
permalink: /posts/2026/04/19/apple-account-change-alerts-abused-to-send-phishing-emails/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement des notifications Apple pour des campagnes de phishing par rappel téléphonique

Des cybercriminels exploitent une vulnérabilité de conception dans les systèmes de notification d'Apple pour envoyer des e-mails frauduleux légitimes, contournant ainsi les filtres anti-spam.

**Points clés :**
* **Méthode d'attaque :** Les attaquants créent un compte Apple et insèrent un message de phishing dans les champs « Nom » et « Prénom ». En modifiant les informations de livraison, ils déclenchent une notification de sécurité automatique envoyée par Apple.
* **Légitimité apparente :** L'e-mail est envoyé directement depuis l'infrastructure d'Apple (`appleid@id.apple.com`) et valide toutes les vérifications d'authentification (SPF, DKIM, DMARC), le rendant indétectable par les solutions de sécurité classiques.
* **Technique de « callback phishing » :** Le message informe la victime d'un achat fictif (ex: un iPhone à 899 $) et l'incite à appeler un numéro pour annuler la transaction. Une fois en ligne, les escrocs tentent de voler des données bancaires ou d'installer des logiciels d'accès à distance.
* **Exploitation :** L'attaque repose sur le détournement des champs de profil utilisateur, inclus dynamiquement par Apple dans ses alertes de sécurité légitimes.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique, car il s'agit d'un abus de fonctionnalité (« abuse of feature ») liée à l'injection de texte utilisateur dans des notifications système automatisées.

**Recommandations :**
* **Méfiance envers les notifications urgentes :** Ne jamais appeler de numéros de téléphone inclus dans des e-mails de notification de sécurité non sollicités.
* **Vérification via les canaux officiels :** Si une alerte semble suspecte, accédez directement au site officiel d'Apple (appleid.apple.com) via un navigateur, sans cliquer sur les liens contenus dans l'e-mail.
* **Vigilance accrue :** Soyez sceptique face aux messages demandant une action immédiate ou impliquant des transactions financières imprévues.

---
[Source](https://www.bleepingcomputer.com/news/security/apple-account-change-alerts-abused-to-send-phishing-emails/){:target="_blank"}
