---
title: 'CISA Warns Fortinet Customers as FortiBleed Hits 86,644 FortiGate Devices'
date: 2026-06-19
permalink: /posts/2026/06/19/cisa-warns-fortinet-customers-as-fortibleed-hits-86644-fortigate-devices/
tags:
- veille-cyber
- hackernews
---
### Campagne « FortiBleed » : Vulnérabilités critiques des équipements Fortinet

La CISA a alerté sur une campagne d'envergure, baptisée **FortiBleed**, visant les passerelles VPN et pare-feux FortiGate exposés sur Internet. Plus de 86 000 appareils ont été compromis mondialement, principalement dans les secteurs des télécommunications, de l'administration et de l'éducation.

**Points clés :**
*   **Méthode d'attaque :** Les acteurs de la menace utilisent des outils automatisés pour tester des combinaisons d'identifiants (brute-force et *credential stuffing*) sur les interfaces d'administration. Une fois l'accès obtenu, ils surveillent le trafic réseau pour collecter davantage de justificatifs.
*   **Origine des identifiants :** La majorité des accès repose sur des comptes par défaut non renommés ou des mots de passe recyclés provenant de fuites antérieures.
*   **Facteur aggravant :** L'utilisation persistante d'anciens mécanismes de hachage SHA-256 (pré-PBKDF2) facilite la compromission des comptes administrateurs sur les versions antérieures à FortiOS 7.2.11, 7.4.8 et 7.6.1.

**Vulnérabilités :**
*   **Exposition des interfaces :** Les services d'administration et VPN accessibles directement depuis Internet.
*   **Faiblesse cryptographique :** Conservation des anciens hashs SHA-256 pour les mots de passe administrateur après une mise à jour, rendant les comptes vulnérables jusqu'à une réinitialisation manuelle.
*   **Mauvaise hygiène de sécurité :** Absence de rotation des mots de passe, usage de comptes par défaut et absence d'authentification multi-facteurs (MFA).

**Recommandations :**
*   **Réinitialisation immédiate :** Fermer les sessions actives, réinitialiser tous les mots de passe administrateur et VPN, et appliquer des politiques de mots de passe robustes.
*   **Durcissement cryptographique :** Forcer l'utilisation de l'algorithme **PBKDF2** pour le stockage des mots de passe administrateur.
*   **Sécurisation des accès :** Implémenter une authentification multi-facteurs (MFA) résistante au phishing sur tous les portails externes.
*   **Surveillance :** Analyser les journaux de connexion et de configuration à la recherche d'activités suspectes.
*   **Réduction de la surface :** Restreindre strictement l'accès aux interfaces d'administration et aux passerelles VPN.

---
[Source](https://thehackernews.com/2026/06/cisa-warns-fortinet-customers-as.html){:target="_blank"}
