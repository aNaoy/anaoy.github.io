---
title: 'Scattered Spider Hackers Plead Guilty on Day 1 of Trial'
date: 2026-06-23
permalink: /posts/2026/06/23/scattered-spider-hackers-plead-guilty-on-day-1-of-trial/
tags:
- veille-cyber
- krebs
---
### Condamnation des membres clés du groupe Scattered Spider

Deux membres éminents du collectif de cybercriminalité **Scattered Spider**, Thalha Jubair (20 ans) et Owen Flowers (18 ans), ont plaidé coupables devant la justice britannique pour leur implication dans des cyberattaques majeures, notamment contre *Transport for London*. Ce groupe est responsable de multiples intrusions à travers le monde, cumulant plus de 115 millions de dollars de rançons extorquées.

**Points clés :**
* **Responsabilités :** Le groupe est impliqué dans des attaques contre des secteurs critiques (santé, transports, hôtellerie/casinos). Jubair gérait notamment le canal Telegram « Star Chat », spécialisé dans le *SIM-swapping*.
* **Mode opératoire :** Utilisation intensive du *phishing* (SMS et voix) pour voler des identifiants et contourner l'authentification multifacteur (MFA). Ils exploitaient également de fausses « demandes de données d'urgence » (*Emergency Data Requests* - EDR) en usurpant des adresses email officielles pour soutirer des informations aux entreprises technologiques.
* **Impact :** Des dizaines d'entreprises renommées (LastPass, DoorDash, Mailchimp, MGM Resorts, etc.) ont été compromises, entraînant des vols de données et des pertes financières massives.

**Vulnérabilités exploitées :**
* **Facteur humain :** L'article souligne une exploitation constante des employés via l'ingénierie sociale (SMS/Phishing) pour obtenir des accès initiaux.
* **Failles de processus :** Abus des procédures d'authentification des opérateurs télécoms (SIM-swapping) et des protocoles de demande de données d'urgence auprès des entreprises technologiques.
* *Note : Aucune CVE spécifique n'est mentionnée, les attaques reposant principalement sur l'usurpation d'identité et l'ingénierie sociale plutôt que sur des vulnérabilités logicielles de type "zero-day".*

**Recommandations :**
* **Renforcement du MFA :** Abandonner l'authentification par SMS ou appels vocaux au profit de clés de sécurité physiques (FIDO2) ou d'applications d'authentification robustes, résistantes au phishing.
* **Vérification des accès :** Mettre en place des processus de vérification stricts et multicanaux pour les demandes de données urgentes (EDR) provenant de forces de l'ordre.
* **Sécurisation des processus télécoms :** Sensibiliser les employés des opérateurs mobiles aux techniques de *SIM-swapping* et durcir les procédures de transfert de numéros de téléphone.
* **Formation continue :** Sensibiliser les collaborateurs aux campagnes de phishing sophistiquées ciblant les identifiants de connexion aux services internes (SSO).

---
[Source](https://krebsonsecurity.com/2026/06/scattered-spider-hackers-plead-guilty-on-day-1-of-trial/){:target="_blank"}
