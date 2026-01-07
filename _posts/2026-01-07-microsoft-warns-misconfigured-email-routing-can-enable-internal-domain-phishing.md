---
title: 'Microsoft Warns Misconfigured Email Routing Can Enable Internal Domain Phishing'
date: 2026-01-07
permalink: /posts/2026/01/07/microsoft-warns-misconfigured-email-routing-can-enable-internal-domain-phishing/
tags:
- veille-cyber
- hackernews
---
**Les Malwares de Spoofing Exploitant les Mauvaises Configurations d'Envoi d'Emails**

Des acteurs malveillants tirent parti de configurations d'envoi d'e-mails complexes et de protections anti-usurpation laxistes pour se faire passer pour des organisations, envoyant des courriels qui semblent provenir de sources internes. Cette tactique, observée en hausse depuis mai 2025, utilise des plateformes de type "Phishing-as-a-Service" (PhaaS), notamment le kit Tycoon 2FA. Les attaques visent à voler des identifiants pour des actions ultérieures telles que le vol de données ou des compromissions de messagerie professionnelle (BEC).

Les scénarios à risque impliquent généralement un routage d'e-mails passant par des environnements Exchange sur site ou des services tiers avant d'atteindre Microsoft 365, en particulier lorsque les enregistrements MX ne pointent pas directement vers Office 365 et que les protections anti-usurpation ne sont pas rigoureusement appliquées. Les e-mails frauduleux se font passer pour des notifications internes, des documents partagés, des communications RH, des réinitialisations de mot de passe, ou des escroqueries financières avec de fausses factures et des documents falsifiés.

**Points Clés:**

*   Les attaquants exploitent les configurations d'envoi d'e-mails complexes et les protections anti-usurpation mal configurées.
*   L'objectif est de tromper les utilisateurs en leur faisant croire que les e-mails proviennent de l'intérieur de leur organisation.
*   Le kit Tycoon 2FA est fréquemment utilisé dans ces campagnes.
*   Les attaques peuvent mener au vol d'identifiants, au vol de données et aux compromissions de messagerie professionnelle (BEC).
*   Les scénarios impliquant des transferts d'e-mails via des services tiers avant Microsoft 365 sont particulièrement vulnérables.

**Vulnérabilités:**

*   Mauvaise configuration des protections anti-usurpation d'e-mails (par exemple, DMARC et SPF).
*   Routage complexe d'e-mails impliquant des services intermédiaires.
*   Absence de politiques DMARC en mode rejet et de politiques SPF en mode "hard fail".

**Recommandations:**

*   Mettre en place des politiques DMARC strictes en mode rejet.
*   Configurer les politiques SPF en mode "hard fail".
*   Configurer correctement les connecteurs tiers pour le filtrage du spam et l'archivage.
*   Désactiver la fonction "Direct Send" si elle n'est pas nécessaire.
*   Veiller à ce que les enregistrements MX pointent directement vers Office 365 pour les locataires utilisant ce service.

---
[Source](https://thehackernews.com/2026/01/microsoft-warns-misconfigured-email.html){:target="_blank"}
