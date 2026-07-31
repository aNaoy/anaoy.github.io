---
title: 'South Korea fines telco giant KT $39 million for customer data breach'
date: 2026-07-31
permalink: /posts/2026/07/31/south-korea-fines-telco-giant-kt-39-million-for-customer-data-breach/
tags:
- veille-cyber
- bleepingcomp
---
### Sanction record pour KT après une compromission prolongée de données

L'opérateur sud-coréen KT Corporation a écopé d'une amende de 39 millions de dollars après la découverte d'une intrusion massive ayant duré 11 mois (octobre 2024 - septembre 2025). L'enquête a révélé l'exposition des données personnelles de 16 647 abonnés et des fraudes aux micro-paiements pour un préjudice de 167 400 $.

**Points clés :**
*   **Vecteur d'attaque physique :** L'utilisation d'une station de base "femtocell" perdue par KT, dont le certificat d'authentification valide a été récupéré pour simuler une cellule légitime sur le réseau.
*   **Malware BPFDoor :** Découverte d'une compromission sur 38 serveurs IT par le backdoor *BPFDoor* dès mars 2024. KT a dissimulé cette infection aux autorités et a détruit des logs critiques durant l'inspection, empêchant d'évaluer l'ampleur totale du vol de données.
*   **Groupement cyber :** Les activités liées au malware ont été associées au groupe d'espionnage *Red Menshen* (lié à la Chine).

**Vulnérabilités identifiées :**
*   **Gestion des certificats :** Durée de validité excessive des certificats femtocell (10 ans).
*   **Contrôles réseau :** Absence de restriction des connexions par IP source et existence de routes contournant le serveur de gestion.
*   **BPFDoor :** Utilisation de la technologie *Berkeley Packet Filter* pour intercepter le trafic de manière passive sans ouvrir de ports, contournant ainsi les pare-feux.

**Recommandations :**
*   **Renforcement matériel :** Mettre en œuvre des contrôles de sécurité stricts pour les équipements de télécommunication (femtocells).
*   **Gouvernance :** Accroître le pouvoir de supervision du responsable de la protection des données (CPO).
*   **Conformité :** Étendre la certification ISMS-P à l'ensemble des systèmes de réseau mobile.
*   **Transparence :** Aligner les protocoles de gestion d'incidents sur les exigences légales pour éviter la destruction de preuves et garantir la notification rapide des autorités.

---
[Source](https://www.bleepingcomputer.com/news/security/south-korea-fines-telco-giant-kt-39-million-for-customer-data-breach/){:target="_blank"}
