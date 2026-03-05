---
title: 'Hacker mass-mails HungerRush extortion emails to restaurant patrons'
date: 2026-03-05
permalink: /posts/2026/03/05/hacker-mass-mails-hungerrush-extortion-emails-to-restaurant-patrons/
tags:
- veille-cyber
- bleepingcomp
---
**Tentative d'extorsion via email ciblant les clients de restaurants utilisant HungerRush**

Des clients de restaurants utilisant la plateforme de point de vente (POS) HungerRush ont reçu des courriels d'un acteur malveillant cherchant à extorquer l'entreprise. Ces courriels menacent de divulguer des données de restaurants et de clients si HungerRush ne répond pas aux demandes. L'attaquant prétend avoir accès à des millions d'enregistrements clients contenant des informations sensibles telles que noms, courriels, mots de passe, adresses, numéros de téléphone, dates de naissance et informations de carte de crédit.

Les courriels ont été envoyés en utilisant l'infrastructure de Twilio SendGrid, une plateforme légitime utilisée par HungerRush pour l'envoi de reçus transactionnels, et ont passé les contrôles d'authentification SPF, DKIM et DMARC pour le domaine hungerrush.com.

Une analyse menée par Hudson Rock suggère qu'un appareil d'un employé de HungerRush aurait été compromis en octobre 2025 par un logiciel malveillant voleur d'informations (infostealer), entraînant le vol de multiples identifiants d'entreprise pour divers services. Il n'est pas encore confirmé si ces identifiants volés sont directement liés à la fuite de données alléguée chez HungerRush.

**Points Clés :**

*   Des courriels d'extorsion ont été envoyés aux clients de restaurants utilisant la plateforme HungerRush.
*   L'attaquant menace de divulguer des données client si ses demandes ne sont pas satisfaites.
*   Les courriels semblaient provenir de sources légitimes de HungerRush (adresses email et infrastructure d'envoi).
*   Une possible compromission d'identifiants d'entreprise via un infostealer a été rapportée, mais le lien direct avec cet incident n'est pas confirmé.

**Vulnérabilités :**

*   Il n'y a pas de CVE (Common Vulnerabilities and Exposures) spécifiquement mentionnée dans l'article pour l'exploitation directe de HungerRush. La vulnérabilité initiale semble être une compromission d'identifiants d'un employé via un infostealer. L'exploitation subséquente exploite la confiance des clients dans les communications de HungerRush et les informations potentiellement dérobées.

**Recommandations :**

*   Les clients de restaurants utilisant le système POS HungerRush doivent être vigilants face aux potentiels courriels et SMS de phishing qui pourraient utiliser les informations prétendument volées.
*   Une enquête approfondie est nécessaire pour confirmer la nature et l'étendue d'une éventuelle violation de données chez HungerRush.
*   Les entreprises utilisant des plateformes comme HungerRush doivent renforcer la sécurité de leurs employés et de leurs systèmes pour prévenir de futures compromissions d'identifiants.

---
[Source](https://www.bleepingcomputer.com/news/security/hacker-mass-mails-hungerrush-extortion-emails-to-restaurant-patrons/){:target="_blank"}
