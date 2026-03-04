---
title: 'Hacker mass-mails HungerRush extortion emails to restaurant patrons'
date: 2026-03-04
permalink: /posts/2026/03/04/hacker-mass-mails-hungerrush-extortion-emails-to-restaurant-patrons/
tags:
- veille-cyber
- bleepingcomp
---
## Tentative d'extorsion ciblant les clients de restaurants utilisant HungerRush

Des clients de restaurants utilisant la plateforme de point de vente (POS) HungerRush ont reçu des courriels d'un acteur malveillant. Ces messages menacent de divulguer des données de restaurants et de leurs clients si HungerRush ne répond pas à leurs demandes.

HungerRush est un fournisseur de technologies pour restaurants, proposant des solutions pour la gestion des commandes, des informations clients et des opérations commerciales. L'entreprise affirme travailler avec plus de 16 000 établissements.

Les courriels, envoyés depuis des adresses semblant légitimes de HungerRush (support@hungerrush.com et 2019@hungerrush.com), prétendent détenir des données sur des millions de clients, incluant noms, courriels, mots de passe, adresses, numéros de téléphone, dates de naissance et informations de carte de crédit. Les en-têtes des courriels indiquent qu'ils ont été envoyés via la plateforme Twilio SendGrid, utilisée précédemment par HungerRush pour des reçus clients, et ont passé les authentifications SPF, DKIM et DMARC du domaine hungerrush.com.

Des signalements sur Reddit corroborent la réception de ces messages, les clients identifiant HungerRush comme le système utilisé par leurs restaurants. Des analyses préliminaires suggèrent qu'un appareil d'un employé de HungerRush aurait pu être compromis en octobre 2025 par un logiciel malveillant voleur d'informations (infostealer), menant au vol de multiples identifiants d'entreprise. L'existence d'une corrélation directe entre ces identifiants volés et la violation de données revendiquée n'est pas encore confirmée.

**Points clés :**

*   Des clients de restaurants utilisant HungerRush reçoivent des courriels d'extorsion.
*   Les courriels menacent de divulguer des données clients si HungerRush ne réagit pas.
*   Les messages semblent provenir du domaine HungerRush et ont passé les authentifications.
*   Une possible compromission d'un employé de HungerRush et le vol d'identifiants sont suspectés.

**Vulnérabilités :**

*   Il est suggéré qu'un employé a été infecté par un "infostealer", menant à la compromission d'identifiants d'entreprise pour des services tels que NetSuite, QuickBooks, Stripe, Bill.com, Visa Online et Salesforce. Aucune CVE spécifique n'est mentionnée dans l'article.

**Recommandations :**

*   Les clients des restaurants utilisant le système HungerRush doivent être vigilants face à d'éventuels courriels ou SMS de phishing exploitant les informations potentiellement compromises.

---
[Source](https://www.bleepingcomputer.com/news/security/hacker-mass-mails-hungerrush-extortion-emails-to-restaurant-patrons/){:target="_blank"}
