---
title: 'WhatsApp Worm Spreads Astaroth Banking Trojan Across Brazil via Contact Auto-Messaging'
date: 2026-01-08
permalink: /posts/2026/01/08/whatsapp-worm-spreads-astaroth-banking-trojan-across-brazil-via-contact-auto-messaging/
tags:
- veille-cyber
- hackernews
---
**Vers Android, l'Astaroth s'infiltre via WhatsApp**

Une nouvelle campagne de cybercriminalité, surnommée "Boto Cor-de-Rosa", exploite WhatsApp pour propager le cheval de Troie bancaire Astaroth, ciblant principalement le Brésil. Ce malware, actif depuis 2015 et connu pour cibler l'Amérique Latine, utilise désormais la popularité de WhatsApp pour se diffuser.

**Points Clés :**

*   **Vecteur de propagation :** Messages WhatsApp contenant des archives ZIP.
*   **Mécanisme de propagation :** Un module en Python récupère la liste de contacts de la victime sur WhatsApp et auto-envoie le fichier malveillant aux contacts, créant un effet de ver.
*   **Charge utile :** Le cheval de Troie bancaire Astaroth, écrit en Delphi, vole des identifiants bancaires en surveillant l'activité de navigation et en ciblant les sites bancaires.
*   **Tactic nouvelle :** L'utilisation de WhatsApp comme canal de distribution pour des chevaux de Troie bancaires est une tactique émergente au Brésil.
*   **Suivi des attaques :** Des campagnes précédentes, comme STAC3150, ont également utilisé cette méthode.
*   **Analyse par les attaquants :** Le malware inclut un mécanisme pour suivre et rapporter les métriques de propagation.

**Vulnérabilités :**

L'article ne mentionne pas de vulnérabilités spécifiques avec des identifiants CVE. La diffusion repose sur l'ingénierie sociale et l'exploitation de la confiance des utilisateurs à l'égard des messages reçus via des plateformes de messagerie populaires.

**Recommandations :**

*   Faire preuve de prudence face aux messages inattendus sur WhatsApp, même s'ils proviennent de contacts connus.
*   Éviter d'ouvrir les pièces jointes provenant de sources non fiables ou non sollicitées.
*   Maintenir les logiciels de sécurité à jour.

---
[Source](https://thehackernews.com/2026/01/whatsapp-worm-spreads-astaroth-banking.html){:target="_blank"}
