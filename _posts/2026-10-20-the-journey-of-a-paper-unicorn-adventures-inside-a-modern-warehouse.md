---
title: 'The journey of a paper unicorn: adventures inside a modern warehouse'
date: 2026-10-20
permalink: /posts/2026/10/20/the-journey-of-a-paper-unicorn-adventures-inside-a-modern-warehouse/
tags:
- veille-cyber
- securelist
---
### Sécurisation des entrepôts logistiques : le défi de l'interconnectivité

Un entrepôt moderne est un écosystème hybride où les processus physiques (convoyeurs, robots) sont pilotés par des flux de données (WMS, Wi-Fi, terminaux). La rupture de cette chaîne numérique entraîne des conséquences concrètes : arrêts de production, erreurs d'inventaire et pertes financières.

**Points clés :**
*   **Système central (WMS) :** Le *Warehouse Management System* est le cerveau de l'entrepôt. Son compromission permet de corrompre l'intégralité du processus logistique, de la réception à l'expédition.
*   **Surface d'attaque étendue :** La convergence entre l'informatique (IT) et les systèmes industriels (OT) crée des failles exploitables à distance (internet), par proximité (Wi-Fi, Bluetooth) ou physiquement (câblage réseau non supervisé).
*   **Risque de intégrité :** La manipulation des données (inventaire, adresses de livraison) est une menace critique car elle désynchronise le monde physique du système d'information.

**Vulnérabilités identifiées :**
*   **Terminaux portables (PDT) :** Le contournement du « mode kiosque » permet l'accès au système d'exploitation et aux réseaux internes.
*   **Scanners de codes-barres :** Injection de commandes malveillantes via des codes QR/barres piégés ou via Bluetooth (ex: **CVE-2026-4272** sur terminaux Honeywell).
*   **Imprimantes thermiques :** Possibilité d'exécution de code arbitraire via des connexions Bluetooth non sécurisées (ex: Zebra ZQ630).
*   **Logiciels de gestion (WMS) :** Vulnérabilités web classiques (injections SQL, contournement d'autorisation comme la **CVE-2026-70774** dans Oracle WMS) permettant une prise de contrôle totale.

**Recommandations :**
*   **Architecture réseau :** Appliquer une segmentation stricte entre l'IT, l'OT, les systèmes de gestion et les réseaux externes (Zero Trust).
*   **Sécurisation des accès :** Implémenter l'authentification IEEE 802.1X et désactiver les ports Ethernet inutilisés dans les zones de stockage.
*   **Gestion des terminaux :** Inclure les scanners, PDT et imprimantes dans le cycle de gestion des correctifs (patch management) et effectuer des tests d'intrusion spécifiques.
*   **Hygiène radiofréquence :** Réaliser des études de couverture RF pour identifier les fuites de signaux vers l'extérieur du site.
*   **Sécurité du personnel :** Mettre en place des contrôles d'accès physiques et logiques renforcés, même pour le personnel temporaire, en limitant les droits au strict nécessaire.
*   **Cycle de vie sécurisé (SSDLC) :** Gouverner les applications WMS par des audits de code et des tests de sécurité réguliers.

---
[Source](https://securelist.com/paper-unicorn-warehouse-security/121537/){:target="_blank"}
