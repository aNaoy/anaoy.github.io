---
title: 'Marquis: Ransomware gang stole data of 672K people in cyberattack'
date: 2026-03-19
permalink: /posts/2026/03/19/marquis-ransomware-gang-stole-data-of-672k-people-in-cyberattack/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque chez Marquis : 672 000 données personnelles compromises

En août 2025, le fournisseur de services financiers Marquis a subi une attaque par ransomware ayant entraîné le vol des données de 672 075 personnes. Cette intrusion a également perturbé les opérations de 74 institutions bancaires américaines utilisant ses services.

**Points clés :**
*   **Nature du vol :** Les attaquants ont exfiltré des informations hautement sensibles : noms, dates de naissance, adresses, numéros de sécurité sociale, numéros d'identification fiscale et détails de comptes financiers.
*   **Origine de l'intrusion :** L'attaque a été rendue possible par la compromission d'un pare-feu SonicWall.
*   **Conséquences juridiques :** Marquis a intenté un procès à SonicWall pour négligence, alléguant que la faille dans le service de sauvegarde cloud du fournisseur a permis l'intrusion. L'entreprise fait actuellement face à plus de 36 recours collectifs de la part des victimes.

**Vulnérabilités :**
*   Le vecteur d'attaque exploite une faille dans le service de sauvegarde cloud de **MySonicWall** (signalée initialement en septembre 2025). Cet incident a permis aux attaquants de dérober des identifiants et des jetons d'accès, facilitant la prise de contrôle des pare-feu des clients.

**Recommandations :**
*   **Gestion des identifiants :** En cas de compromission signalée par un fournisseur de services réseau, il est impératif de réinitialiser immédiatement toutes les informations d'identification associées (compte MySonicWall, accès administrateur).
*   **Hygiène des accès :** Appliquer une authentification multifacteur (MFA) robuste sur tous les équipements périmétriques et points d'administration.
*   **Audit de sécurité des tiers :** Renforcer la surveillance des accès fournis par des prestataires tiers et s'assurer de la réactivité des fournisseurs en cas de vulnérabilité identifiée sur leurs infrastructures.

---
[Source](https://www.bleepingcomputer.com/news/security/marquis-ransomware-gang-stole-data-of-672-000-people-in-2025-cyberattack/){:target="_blank"}
