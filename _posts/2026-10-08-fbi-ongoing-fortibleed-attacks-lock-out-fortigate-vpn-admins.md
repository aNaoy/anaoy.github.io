---
title: 'FBI: Ongoing FortiBleed attacks lock out FortiGate VPN admins'
date: 2026-10-08
permalink: /posts/2026/10/08/fbi-ongoing-fortibleed-attacks-lock-out-fortigate-vpn-admins/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne « FortiBleed » : Menace persistante sur les passerelles FortiGate

Le FBI alerte sur la poursuite des attaques « FortiBleed » visant les pare-feu et passerelles VPN FortiGate exposés. Cette campagne, exploitant une fuite massive de près de 87 000 identifiants, permet aux attaquants de prendre le contrôle total des équipements et de verrouiller les administrateurs légitimes.

**Points clés**
* **Mode opératoire :** Les attaquants utilisent des identifiants compromis (fuites, *infostealers*, *credential stuffing*) pour accéder aux appareils, extraire des données d'authentification, puis casser les hashs hors ligne via des clusters GPU (Hashcat).
* **Impact :** Les assaillants suppriment les comptes administrateurs existants ou modifient leurs mots de passe, assurant ainsi la persistance et facilitant le mouvement latéral.
* **Finalité :** L'accès est souvent utilisé comme point d'entrée pour le déploiement de ransomwares (groupes INC/Lynx et Payload).
* **Outils :** Les attaquants automatisent le scan des portails SSL VPN, filtrent les honeypots et priorisent leurs cibles selon le revenu et la structure réseau de l'organisation.

**Vulnérabilités**
* Exploitation de configurations VPN compromises et faiblesse des algorithmes de hachage de mots de passe (SHA-256 legacy). *Note : Aucune CVE spécifique n'est citée, l'attaque repose principalement sur l'exploitation d'identifiants volés et une mauvaise gestion des accès.*

**Recommandations**
* **Gestion des accès :** Restreindre l'accès externe aux interfaces d'administration et renforcer le contrôle des accès VPN.
* **Authentification :** Imposer l'authentification multifacteur (MFA) sur tous les accès.
* **Sécurité des mots de passe :** Utiliser l'algorithme PBKDF2 pour le stockage des mots de passe administrateur afin de contrer le cassage par force brute hors ligne.
* **Remédiation :** Réinitialiser les mots de passe de tous les comptes, terminer les sessions VPN actives et auditer minutieusement les journaux d'activité à la recherche de modifications non autorisées.

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-ongoing-fortibleed-attacks-lock-out-fortigate-vpn-admins/){:target="_blank"}
