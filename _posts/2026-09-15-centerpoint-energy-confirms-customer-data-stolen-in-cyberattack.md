---
title: 'CenterPoint Energy confirms customer data stolen in cyberattack'
date: 2026-09-15
permalink: /posts/2026/09/15/centerpoint-energy-confirms-customer-data-stolen-in-cyberattack/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données massive chez CenterPoint Energy

CenterPoint Energy, fournisseur majeur d'électricité et de gaz aux États-Unis, a confirmé une violation de données ayant entraîné l'exfiltration d'informations personnelles de ses clients. Un acteur malveillant affirme avoir dérobé 7,49 millions d'enregistrements en exploitant une vulnérabilité dans une interface de programmation (API) publique de l'entreprise.

**Points clés :**
* **Nature de l'incident :** Accès non autorisé via un système externe exposé, ayant permis l'extraction massive de données clients (noms, adresses, numéros de téléphone, numéros de compte et numéros de sécurité sociale partiels).
* **Mode opératoire :** L'attaquant a utilisé une technique d'énumération automatisée sur l'API publique de l'entreprise.
* **Impact opérationnel :** Les services de distribution d'énergie n'ont pas été affectés.
* **Conséquences juridiques :** Plusieurs recours collectifs (*class actions*) ont été déposés contre l'entreprise.

**Vulnérabilités exploitées :**
* **Absence de limitation de débit (*Rate Limiting*) :** L'API ne restreignait pas le nombre de requêtes, permettant une itération massive sur les identifiants.
* **Défaut de protection WAF :** L'absence de pare-feu applicatif a permis l'automatisation des accès malveillants.
* *Note : Aucune référence CVE n'est associée à cet incident, il s'agit d'une vulnérabilité de conception et de configuration de l'API.*

**Recommandations de sécurité :**
* **Sécurisation des API :** Implémenter strictement des mécanismes de limitation de débit (*rate limiting*) et d'authentification robuste pour empêcher le moissonnage de données.
* **Protection périmétrique :** Déployer et configurer correctement des pare-feu d'applications web (WAF) pour détecter et bloquer les comportements automatisés suspects.
* **Surveillance et journalisation :** Mettre en place une surveillance en temps réel des flux API pour identifier rapidement les tentatives d'énumération ou d'accès anormal.
* **Audit de sécurité :** Réaliser régulièrement des tests d'intrusion et des audits sur l'ensemble des points d'entrée exposés sur Internet.

---
[Source](https://www.bleepingcomputer.com/news/security/centerpoint-energy-confirms-customer-data-stolen-in-cyberattack/){:target="_blank"}
