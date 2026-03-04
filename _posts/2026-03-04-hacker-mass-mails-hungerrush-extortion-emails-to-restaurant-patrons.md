---
title: 'Hacker mass-mails HungerRush extortion emails to restaurant patrons'
date: 2026-03-04
permalink: /posts/2026/03/04/hacker-mass-mails-hungerrush-extortion-emails-to-restaurant-patrons/
tags:
- veille-cyber
- bleepingcomp
---
## Campagne d'extorsion ciblant les clients de HungerRush

Des clients de restaurants utilisant la plateforme de point de vente (POS) HungerRush ont reçu des courriels d'extorsion affirmant que des données de restaurants et de clients sont menacées. Les messages proviennent d'adresses email apparemment liées à HungerRush, notamment support@hungerrush.com et 2019@hungerrush.com, et avertissent de la mise en péril de données personnelles (noms, emails, mots de passe, adresses, numéros de téléphone, dates de naissance, informations de carte de crédit) si les demandes ne sont pas satisfaites.

L'analyse des en-têtes des courriels révèle qu'ils ont été envoyés via Twilio SendGrid, un service utilisé par HungerRush pour l'envoi de reçus transactionnels. Les courriels ont réussi les authentifications SPF, DKIM et DMARC pour le domaine hungerrush.com, indiquant une utilisation légitime du service d'envoi par le domaine de l'entreprise.

Des rapports sur Reddit indiquent que les destinataires ont identifié HungerRush comme leur fournisseur POS par le passé. Une enquête suggère qu'un appareil d'un employé de HungerRush aurait été compromis en octobre 2025 par un logiciel malveillant voleur d'informations, entraînant le vol d'identifiants corporatifs pour divers services critiques, bien qu'un lien direct avec la fuite de données signalée reste incertain.

### Points clés :

*   Des courriels d'extorsion sont envoyés à des clients de restaurants utilisant HungerRush.
*   Les attaquants menacent de divulguer des données de millions de clients.
*   Les courriels semblent utiliser des adresses email légitimes de HungerRush et passent les authentifications de domaine.
*   L'hypothèse d'une compromission des identifiants d'un employé de HungerRush est évoquée.

### Vulnérabilités :

*   Non spécifié dans l'article. L'article suggère une possible compromission des identifiants d'un employé, mais sans attribution de CVE spécifique.

### Recommandations :

*   Les clients des restaurants utilisant le système POS HungerRush doivent être vigilants quant à d'éventuels courriels et SMS d'hameçonnage exploitant les informations prétendument volées.

---
[Source](https://www.bleepingcomputer.com/news/security/hacker-mass-mails-hungerrush-extortion-emails-to-restaurant-patrons/){:target="_blank"}
