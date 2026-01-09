---
title: 'Cisco switches hit by reboot loops due to DNS client bug'
date: 2026-01-09
permalink: /posts/2026/01/09/cisco-switches-hit-by-reboot-loops-due-to-dns-client-bug/
tags:
- veille-cyber
- bleepingcomp
---
**Des commutateurs Cisco bloqués dans des boucles de redémarrage à cause d'un bug DNS**

Plusieurs modèles de commutateurs Cisco rencontrent des boucles de redémarrage intempestives suite à des erreurs fatales du client DNS intégré. Ce problème, qui semble être déclenché globalement ou par une condition temporelle, provoque des redémarrages répétés après une tentative de résolution de "www.cisco.com" ou de serveurs NTP.

**Points Clés :**

*   Des erreurs DNS fatales entraînent des boucles de redémarrage sur une gamme de commutateurs Cisco.
*   Le problème affecte le service client DNS (DNSC) du firmware des appareils.
*   Les redémarrages se produisent toutes les quelques minutes, perturbant gravement les opérations réseau.
*   Plusieurs administrateurs ont constaté l'apparition simultanée des erreurs sur différents réseaux.

**Vulnérabilités :**

Aucun identifiant CVE spécifique n'a été attribué à ce problème au moment de la rédaction. L'erreur est décrite comme suit dans les journaux :
`DNS_CLIENT - SRCADDRFAIL - Result is 2. Failed to identify address for specified name 'www.cisco.com.', requested addr type 2. ***** FATAL ERROR ***** Reporting Task: DNSC.`

**Appareils Affectés :**

*   Cisco CBS250 series
*   Cisco CBS350 series (incluant le CBS350-24P-4G)
*   Cisco Catalyst C1200 series
*   Cisco SG350
*   Cisco SG350X
*   Cisco SG550X series

**Recommandations :**

Des solutions de contournement temporaires ont été identifiées pour interrompre les boucles de redémarrage :

*   Désactiver la résolution DNS sur les commutateurs.
*   Désactiver la synchronisation horaire SNTP ou tout autre service de synchronisation de l'heure.
*   Bloquer l'accès sortant à Internet depuis les interfaces de gestion des commutateurs.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-switches-hit-by-reboot-loops-due-to-dns-client-bug/){:target="_blank"}
