---
title: 'Berlin Refuses to Pay Hackers Who Stole Data From the Citys State Network'
date: 2026-08-29
permalink: /posts/2026/08/29/berlin-refuses-to-pay-hackers-who-stole-data-from-the-citys-state-network/
tags:
- veille-cyber
- hackernews
---
### Cyberattaque contre l'État de Berlin : Refus de paiement et enjeux de sécurité

Le gouvernement de l'État de Berlin est la cible d'une tentative d'extorsion suite à une compromission de son réseau administratif découverte en août 2026. Le groupe de ransomwares **Rhysida** est identifié comme responsable de l'exfiltration de 5,79 To de données (environ 1,44 million de fichiers). Malgré la menace de fuite de données personnelles concernant plus de 12 000 individus, les autorités berlinoises refusent de céder aux exigences des pirates.

#### Points clés
*   **Intrusion :** L'exfiltration a eu lieu entre le 7 et le 12 août 2026, entraînant l'isolement temporaire de plusieurs départements du réseau étatique.
*   **Acteurs :** Le groupe Rhysida, lié à des campagnes de double extorsion, est pointé du doigt. Il s'agit du même acteur ayant ciblé plusieurs entités en Allemagne.
*   **Impact :** La nature exacte des données exfiltrées (fichiers géospatiaux, informations personnelles) est en cours d'analyse. Les services de l'État ont été reconnectés depuis le 23 août.
*   **Événements connexes :** L'article mentionne également une fuite de données clients affectant le groupe aéroportuaire *Manchester Airports Group* (MAG), bien que cet incident soit distinct de l'attaque berlinoise.

#### Vulnérabilités exploitées (Méthodes Rhysida)
Le groupe Rhysida utilise généralement les vecteurs d'attaque suivants :
*   **Accès par identifiants valides :** Exploitation de services distants (VPN) dépourvus d'authentification multifacteur (MFA).
*   **Zerologon (CVE-2020-1472) :** Vulnérabilité d'élévation de privilèges dans le protocole Netlogon de Microsoft.
*   **Phishing :** Utilisation de campagnes d'hameçonnage pour pénétrer les réseaux cibles.

#### Recommandations de sécurité
Selon les agences de cybersécurité (CISA, FBI, MS-ISAC) :
*   **Refus de paiement :** Ne jamais payer de rançon, car cela ne garantit pas la récupération des données et encourage les cybercriminels.
*   **Authentification :** Implémenter l'authentification multifacteur (MFA) par défaut sur tous les services exposés.
*   **Gestion des correctifs :** Prioriser la remédiation des vulnérabilités connues, notamment en mettant à jour les systèmes critiques pour contrer des failles comme CVE-2020-1472.
*   **Segmentation réseau :** Cloisonner les réseaux pour limiter la propagation latérale des malwares en cas d'intrusion.

---
[Source](https://thehackernews.com/2026/08/berlin-refuses-to-pay-hackers-who-stole.html){:target="_blank"}
