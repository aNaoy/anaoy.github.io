---
title: 'Microsoft Store Outlook add-in hijacked to steal 4,000 Microsoft accounts'
date: 2026-02-12
permalink: /posts/2026/02/12/microsoft-store-outlook-add-in-hijacked-to-steal-4000-microsoft-accounts/
tags:
- veille-cyber
- bleepingcomp
---
**Utilisation malveillante d'un module complémentaire Outlook pour le vol de données**

Un module complémentaire légitime pour Outlook, nommé "AgreeTo", initialement conçu pour la planification de réunions, a été détourné par des acteurs malveillants. Ce module, disponible sur le Microsoft Office Add-in Store depuis décembre 2022, a été abandonné par son développeur. L'URL associée au module a ensuite été revendiquée par des cybercriminels, qui l'ont transformée en un outil de phishing sophistiqué.

Ce module malveillant présentait une fausse page de connexion Microsoft aux utilisateurs, dans le but de voler leurs identifiants de compte. Les informations saisies étaient ensuite exfiltrées via une API Telegram vers les attaquants. Pour masquer l'activité, les victimes étaient redirigées vers la véritable page de connexion Microsoft.

Selon les recherches menées par la société de sécurité Koi Security, cette campagne a permis de dérober plus de 4 000 identifiants de comptes Microsoft, ainsi que des numéros de carte bancaire et des réponses à des questions de sécurité. Le module avait conservé des permissions lui permettant de lire et modifier les e-mails des utilisateurs, bien qu'aucune activité de ce type n'ait été confirmée.

Le module a été retiré de la boutique Microsoft le jour de sa découverte. L'opérateur de cette attaque semble également être à l'origine d'autres outils de phishing ciblant divers services.

**Points clés :**

*   Un module complémentaire Outlook légitime (AgreeTo) a été détourné.
*   Le module a été utilisé pour lancer une campagne de phishing ciblant les comptes Microsoft.
*   Plus de 4 000 identifiants de comptes Microsoft ont été volés.
*   Des informations financières et de sécurité ont également été compromises.
*   Le module était hébergé sur le Microsoft Office Add-in Store.

**Vulnérabilités :**

*   Le processus de vérification des modules une fois approuvés par Microsoft semble insuffisant, permettant à un acteur malveillant de prendre le contrôle d'une URL abandonnée et de charger du contenu malveillant depuis son propre serveur.
*   Le module a été approuvé par Microsoft malgré son contenu potentiellement malveillant une fois son URL détournée.

**Recommandations :**

*   Supprimer immédiatement le module complémentaire AgreeTo si installé sur Outlook.
*   Réinitialiser les mots de passe des comptes Microsoft potentiellement compromis.
*   Les utilisateurs doivent faire preuve de vigilance face aux modules complémentaires, même s'ils proviennent de boutiques officielles, et vérifier la légitimité des demandes de connexion.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-store-outlook-add-in-hijacked-to-steal-4-000-microsoft-accounts/){:target="_blank"}
