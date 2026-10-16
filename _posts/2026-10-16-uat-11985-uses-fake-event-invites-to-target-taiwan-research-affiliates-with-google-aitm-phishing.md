---
title: 'UAT-11985 Uses Fake Event Invites to Target Taiwan Research Affiliates With Google AitM Phishing'
date: 2026-10-16
permalink: /posts/2026/10/16/uat-11985-uses-fake-event-invites-to-target-taiwan-research-affiliates-with-google-aitm-phishing/
tags:
- veille-cyber
- hackernews
---
### Campagne de phishing sophistiquée UAT-11985 contre le secteur de la recherche à Taïwan

Le groupe APT **UAT-11985** mène une campagne de spear-phishing ciblée visant les institutions de recherche et universitaires à Taïwan. Les attaquants utilisent l'IA générative pour créer des invitations à des événements factices, impersonnalisant des organisations réputées afin de dérober des identifiants Google et des codes MFA via une architecture **Adversary-in-the-Middle (AitM)**.

#### Points clés
*   **Tactique d'ingénierie sociale :** Utilisation de structures d'e-mails standardisées combinant contexte géopolitique, flatteries personnalisées et détails logistiques d'événements publics.
*   **Quishing (QR code phishing) :** Détournement d'affiches d'événements réelles en remplaçant les QR codes légitimes par des versions malveillantes.
*   **Infrastructure AitM :** Utilisation de serveurs proxy en temps réel qui relaient les interactions entre la victime et les serveurs de Google (via WebSockets), permettant la capture dynamique des identifiants et des jetons MFA sans éveiller les soupçons.
*   **Ciblage linguistique :** Les pages de phishing sont optimisées pour les utilisateurs anglophones et sinophones (chinois traditionnel et simplifié).

#### Vulnérabilités
*   L'attaque ne repose pas sur l'exploitation d'une faille logicielle (CVE) spécifique, mais sur **l'exploitation de la confiance humaine** et la capacité de l'architecture AitM à contourner les mécanismes d'authentification multifacteur (MFA) en interceptant les jetons de session en temps réel.

#### Recommandations
*   **Authentification FIDO2/WebAuthn :** Privilégier les clés de sécurité matérielles (type YubiKey), qui sont les seules à offrir une protection efficace contre les attaques AitM, contrairement aux codes SMS ou aux applications d'authentification classiques.
*   **Vérification des URL :** Systématiser la vérification des URL dans la barre d'adresse avant toute saisie de données, même si l'interface semble identique à celle d'un service légitime.
*   **Méfiance envers les QR codes :** Ne jamais scanner de QR codes provenant de sources non vérifiées ou apposés sur des documents publics/e-mails de manière suspecte.
*   **Sensibilisation :** Former le personnel à reconnaître les structures d'e-mails générées par IA et à vérifier l'identité de l'expéditeur via des canaux de communication officiels avant de s'inscrire à des événements académiques.

---
[Source](https://thehackernews.com/2026/10/uat-11985-uses-fake-event-invites-to.html){:target="_blank"}
