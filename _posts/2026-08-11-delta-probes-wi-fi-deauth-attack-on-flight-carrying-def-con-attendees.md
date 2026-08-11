---
title: 'Delta probes Wi-Fi deauth attack on flight carrying DEF CON attendees'
date: 2026-08-11
permalink: /posts/2026/08/11/delta-probes-wi-fi-deauth-attack-on-flight-carrying-def-con-attendees/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque Wi-Fi malveillante sur un vol Delta : retour de la DEF CON

Delta Air Lines a ouvert une enquête suite à un incident survenu sur le vol 591 reliant Las Vegas à Atlanta. Des passagers, revenant de la conférence de cybersécurité DEF CON, ont été accusés d'avoir compromis la sécurité du réseau Wi-Fi à bord.

**Points clés :**
*   **Mode opératoire :** Les suspects ont réalisé une attaque par déauthentification (deauth) pour déconnecter les autres passagers du réseau officiel, puis ont diffusé un réseau malveillant nommé « Delta WiFi Fast ».
*   **Objectif :** Créer un portail captif frauduleux (phishing) pour dérober des identifiants personnels et des comptes Google.
*   **Réaction :** L'équipage a désactivé le Wi-Fi pendant 30 minutes. À l'atterrissage, des agents fédéraux sont intervenus pour interroger les suspects et saisir leur matériel informatique. La sécurité des systèmes de vol n'a pas été impactée.

**Vulnérabilités :**
*   **Attaque par déauthentification Wi-Fi :** Exploitation du protocole 802.11 qui, dans sa version standard, permet l'envoi de trames de gestion non chiffrées. Un attaquant peut usurper l'adresse MAC du point d'accès légitime pour forcer la déconnexion des clients (attaque de type déni de service).

**Recommandations :**
*   **Utilisation du PMF (Protected Management Frames) :** Les réseaux Wi-Fi doivent activer le standard 802.11w (PMF) pour chiffrer les trames de gestion et empêcher ainsi les attaques par déauthentification ou désassociation.
*   **Vigilance utilisateur :** Ne jamais saisir d'identifiants sur des réseaux Wi-Fi publics non vérifiés ou présentant des certificats SSL/TLS invalides.
*   **Sécurisation des infrastructures :** Les opérateurs de réseaux Wi-Fi publics doivent renforcer la surveillance des points d'accès non autorisés (Rogue AP) pour détecter rapidement toute tentative de clonage de réseau (Evil Twin).

---
[Source](https://www.bleepingcomputer.com/news/security/delta-probes-wi-fi-deauth-attack-on-flight-carrying-def-con-attendees/){:target="_blank"}
