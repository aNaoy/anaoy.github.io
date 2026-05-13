---
title: 'UK fines water supplier $1.3M for exposing data of 664k customers'
date: 2026-05-13
permalink: /posts/2026/05/13/uk-fines-water-supplier-13m-for-exposing-data-of-664k-customers/
tags:
- veille-cyber
- bleepingcomp
---
### Sanction record pour South Staffordshire Water suite à une fuite de données massive

L'autorité britannique de protection des données (ICO) a infligé une amende de 963 900 £ (1,3 million $) à la société South Staffordshire Water après qu'une cyberattaque a exposé les données personnelles de 663 887 clients et employés. Bien que l'intrusion ait débuté par un hameçonnage en septembre 2020, les attaquants ont maintenu une présence persistante dans le réseau pendant 20 mois avant d'exfiltrer les données en 2022.

**Points clés**
* **Nature de la brèche :** Compromission initiale par hameçonnage, suivie d'une élévation de privilèges jusqu'à l'accès administrateur du domaine.
* **Impact :** Exfiltration d'informations sensibles (noms, adresses, coordonnées bancaires, numéros de sécurité sociale, données RH).
* **Détection tardive :** L'intrusion n'a été découverte qu'en juillet 2022 suite à des problèmes de performance informatique, malgré une présence active des pirates depuis 2020.
* **Coopération :** L'amende initiale a été réduite de 40 % en raison de la coopération de l'entreprise et de son admission de responsabilité.

**Vulnérabilités identifiées**
* **Obsolescence logicielle :** Utilisation de systèmes non supportés (ex: Windows Server 2003).
* **Gestion des correctifs :** Défauts majeurs dans le déploiement des mises à jour de sécurité.
* **Surveillance insuffisante :** Seulement 5 % de l'infrastructure informatique était couverte par des outils de monitoring.
* **Contrôle des accès :** absence de mécanismes efficaces pour limiter l'élévation de privilèges.

**Recommandations**
* **Modernisation du parc informatique :** Remplacer systématiquement les logiciels obsolètes par des versions supportées et sécurisées.
* **Extension de la visibilité :** Mettre en place un monitoring complet de l'environnement informatique pour détecter toute activité anormale.
* **Gestion des vulnérabilités :** Instaurer des cycles réguliers de scan de sécurité (internes et externes) et appliquer rigoureusement les correctifs de sécurité.
* **Durcissement des accès :** Implémenter le principe du moindre privilège et sécuriser les comptes à hauts privilèges pour limiter les mouvements latéraux des attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/uk-fines-water-supplier-13m-for-exposing-data-of-664k-customers/){:target="_blank"}
