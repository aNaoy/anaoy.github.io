---
title: 'Hacker mass-mails HungerRush extortion emails to restaurant patrons'
date: 2026-03-04
permalink: /posts/2026/03/04/hacker-mass-mails-hungerrush-extortion-emails-to-restaurant-patrons/
tags:
- veille-cyber
- bleepingcomp
---
**Campagne d'extorsion ciblant des clients de restaurants via des courriels**

Des clients de restaurants utilisant la plateforme de système de point de vente (POS) HungerRush ont reçu des courriels de menace d'un acteur malveillant. Ces courriels affirment détenir des données sensibles de clients et d'entreprises, menaçant de les divulguer si HungerRush ne répond pas à leurs demandes. Les courriels, envoyés depuis des adresses semblant légitimes de HungerRush, ont réussi les contrôles d'authentification des courriels, suggérant une possible compromission de la plateforme d'envoi de courriels de l'entreprise, Twilio SendGrid.

**Points Clés :**

*   Des clients de restaurants utilisant HungerRush ont reçu des courriels d'extorsion.
*   Les courriels menacent de divulguer des données clients et d'entreprise si une demande n'est pas satisfaite.
*   Les courriels ont été envoyés en utilisant l'infrastructure légitime de HungerRush pour l'envoi de courriels, passant les vérifications SPF, DKIM et DMARC.
*   Des indices suggèrent qu'un appareil d'un employé de HungerRush aurait été compromis en octobre 2025 par un logiciel espion (infostealer), entraînant le vol de multiples identifiants d'entreprise.

**Vulnérabilités :**

*   Bien qu'aucun CVE spécifique ne soit mentionné, l'incident suggère une **compromission des identifiants d'entreprise** suite à une infection par un logiciel espion sur le poste d'un employé. Cette compromission aurait permis à l'attaquant d'obtenir un accès aux systèmes de HungerRush ou à ceux de ses fournisseurs.

**Recommandations :**

*   Les clients des restaurants utilisant HungerRush doivent être vigilants face aux potentiels courriels de phishing et SMS frauduleux exploitant les informations prétendument volées.
*   Les organisations utilisant des plateformes similaires devraient renforcer la sécurité de leurs employés, notamment par la détection et la suppression des logiciels malveillants et par une politique de gestion des identifiants rigoureuse.
*   Il est crucial pour HungerRush de confirmer la portée de la brèche, de sécuriser ses systèmes et de communiquer de manière transparente avec ses clients.

---
[Source](https://www.bleepingcomputer.com/news/security/hacker-mass-mails-hungerrush-extortion-emails-to-restaurant-patrons/){:target="_blank"}
