---
title: 'US and South Korea warn of Gunra ransomware targeting govt agencies'
date: 2026-08-11
permalink: /posts/2026/08/11/us-and-south-korea-warn-of-gunra-ransomware-targeting-govt-agencies/
tags:
- veille-cyber
- bleepingcomp
---
### Menace mondiale du ransomware Gunra : Alerte conjointe USA-Corée du Sud

Les autorités américaines et sud-coréennes ont émis une alerte concernant le groupe de ransomware **Gunra**, actif depuis avril 2025. Ce groupe, potentiellement lié au collectif nord-coréen Lazarus, utilise une variante basée sur le code source fuité de **Conti**. Le groupe emploie une stratégie de double extorsion et a professionnalisé ses opérations en lançant un programme de Ransomware-as-a-Service (RaaS) sous l'alias « Golden Community ».

**Points clés :**
*   **Expansion opérationnelle :** Gunra recrute activement des courtiers d'accès initial (initial access brokers) et des testeurs d'intrusion pour cibler divers secteurs (santé, finance, infrastructures critiques).
*   **Multiplateforme :** Initialement limité aux environnements Windows, le groupe déploie désormais des variantes pour systèmes Linux.
*   **Tactiques :** Les attaquants tentent des contacts directs avec le personnel de direction des victimes pour négocier les rançons.

**Vulnérabilités exploitées :**
Le groupe cible principalement les passerelles VPN et les équipements de sécurité exposés sur Internet, notamment :
*   **CVE-2024-55591** : Vulnérabilité d'authentification critique dans FortiOS et FortiProxy.
*   **CVE-2025-24472** : Vulnérabilité d'authentification critique dans FortiOS et FortiProxy.
*   Autres failles liées à l'exposition des identifiants et aux contrôles d'accès SSH sur les passerelles VPN.

**Recommandations de sécurité :**
*   **Mise à jour immédiate :** Appliquer les correctifs pour toutes les vulnérabilités connues sur les systèmes exposés sur Internet.
*   **Segmentation réseau :** Cloisonner les réseaux pour limiter les mouvements latéraux des attaquants en cas de compromission.
*   **Gestion des sauvegardes :** Maintenir des sauvegardes de données hors ligne et sécurisées pour permettre une restauration rapide sans céder au paiement de la rançon.

---
[Source](https://www.bleepingcomputer.com/news/security/us-warns-of-gunra-ransomware-attacks-against-government-critical-infrastructure/){:target="_blank"}
