---
title: 'US and allies warn of Russian critical infrastructure attacks'
date: 2026-07-13
permalink: /posts/2026/07/13/us-and-allies-warn-of-russian-critical-infrastructure-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Menace russe sur les infrastructures critiques : Alerte internationale

Une coalition internationale de neuf agences de cybersécurité (incluant la NSA, le FBI, la CISA et l'ANSSI) a émis une alerte concernant le groupe russe « Centre 16 » (alias *Berserk Bear*, *Dragonfly*). Ces pirates ciblent les infrastructures critiques — notamment l'énergie, la santé, la défense et les télécommunications — en exploitant des routeurs mal configurés ou vulnérables.

**Points clés :**
*   **Méthodes d'attaque :** Utilisation de scans IP pour identifier des routeurs exposés avec des identifiants SNMP par défaut ou faibles.
*   **Exfiltration :** Vol de fichiers de configuration via le protocole TFTP vers des serveurs contrôlés par les attaquants.
*   **Ciblage :** En plus du protocole SNMP, les attaquants exploitent des vulnérabilités connues sur les équipements Cisco.
*   **Contexte élargi :** Cette alerte fait suite au démantèlement récent de la campagne *FrostArmada* (attribuée au groupe APT28), qui avait compromis 18 000 routeurs SOHO via des détournements DNS pour voler des identifiants Microsoft 365.

**Vulnérabilités identifiées :**
*   **CVE-2018-0171 :** Vulnérabilité critique dans la fonctionnalité « Smart Install » des logiciels Cisco IOS et IOS XE.
*   **Faiblesses génériques :** Utilisation de mots de passe et chaînes de communauté SNMP par défaut.

**Recommandations de sécurité :**
*   **Migration :** Passer au protocole SNMPv3, plus sécurisé.
*   **Durcissement :** Désactiver la fonctionnalité Cisco Smart Install et appliquer des mots de passe robustes et uniques.
*   **Filtrage réseau :** Bloquer le trafic TFTP et SNMP au niveau des pare-feu de périphérie.
*   **Maintenance :** Mettre à jour les micrologiciels et remplacer les équipements arrivés en fin de vie (EOL).

---
[Source](https://www.bleepingcomputer.com/news/security/us-and-allies-share-defense-tips-against-russian-hackers-targeting-critical-infrastructure/){:target="_blank"}
