---
title: 'Microsoft Defender flags legitimate Google search links as malicious'
date: 2026-09-02
permalink: /posts/2026/09/02/microsoft-defender-flags-legitimate-google-search-links-as-malicious/
tags:
- veille-cyber
- bleepingcomp
---
### Faux positif massif sur les liens Google dans Microsoft Defender

Microsoft Defender pour Office 365 rencontre actuellement un dysfonctionnement technique provoquant le blocage erroné de liens légitimes issus du moteur de recherche Google. Les utilisateurs tentant d'accéder à ces URL reçoivent une notification de sécurité avertissant que le site « pourrait ne pas être sûr ».

**Points clés :**
* **Origine du problème :** Une classification de sécurité erronée au sein des systèmes de Microsoft Defender.
* **Impact :** Les liens Google sont bloqués systématiquement dans les emails, Teams et les applications Office 365. Le copier-coller du lien ne permet pas de contourner la restriction.
* **Alertes administratives :** Les administrateurs IT peuvent recevoir des notifications de menaces générées par ces faux positifs dans les portails Microsoft Defender et Microsoft Sentinel.
* **Identification :** L'incident est suivi sous la référence **MO1465962**.

**Vulnérabilités :**
* Aucune vulnérabilité (CVE) n'est associée à cet événement ; il s'agit d'une erreur de logique métier dans les algorithmes de filtrage « Safe Links ».

**Recommandations :**
* **Attente active :** Microsoft travaille actuellement à la correction de la classification pour restaurer l'accès normal.
* **Surveillance :** Les administrateurs doivent surveiller le centre de messages Microsoft 365 (référence MO1465962) pour obtenir des mises à jour sur le déploiement du correctif.
* **Gestion des incidents :** Il est conseillé aux équipes de sécurité de vérifier les alertes générées dans Microsoft Sentinel et le portail Defender afin de ne pas mobiliser inutilement des ressources sur ces faux positifs.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-defender-flags-legitimate-google-search-links-as-malicious/){:target="_blank"}
