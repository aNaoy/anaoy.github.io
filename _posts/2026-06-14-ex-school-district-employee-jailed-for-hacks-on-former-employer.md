---
title: 'Ex-school district employee jailed for hacks on former employer'
date: 2026-06-14
permalink: /posts/2026/06/14/ex-school-district-employee-jailed-for-hacks-on-former-employer/
tags:
- veille-cyber
- bleepingcomp
---
# Condamnation pour cybermalveillance interne : Leçons d'un accès non révoqué

Un ancien employé informatique du district scolaire de Saydel (Iowa), Ezekiel Dean Potter, a été condamné à 21 mois de prison pour avoir saboté les systèmes de son ex-employeur pendant plus de 18 mois. Ayant conservé des identifiants d'accès après son départ en avril 2023, il a multiplié les attaques, supprimant des comptes administrateurs (Google, Apple School Manager, réseaux sociaux) et perturbant gravement les activités pédagogiques. Le préjudice financier s'élève à près de 60 000 dollars.

**Points clés :**
*   **Mode opératoire :** Utilisation persistante d'identifiants administrateurs non révoqués, masquage des accès via VPN et stockage d'identifiants dérobés sur des supports externes.
*   **Impact :** Paralysie de la gestion des appareils (iPads/MacBooks), interruption des plateformes d'apprentissage (Schoology) et suppression des comptes emails de la direction.
*   **Détection :** L'enquête a été facilitée par la découverte d'une clé USB contenant des identifiants et par la traçabilité des adresses IP liées à ses employeurs ultérieurs.

**Vulnérabilités exploitées :**
*   **Gestion des accès (IAM) défaillante :** Absence de procédure de révocation immédiate des droits et des accès lors du départ d'un collaborateur (le risque principal dans cette affaire).
*   **Absence d'authentification multifacteur (MFA) robuste :** Le maintien de l'accès via des identifiants simples a permis une compromission prolongée.

**Recommandations :**
*   **Offboarding strict :** Automatiser la désactivation immédiate de tous les comptes, jetons API et accès VPN lors de la fin de contrat d'un collaborateur.
*   **Audit des privilèges :** Réaliser des revues régulières des droits d'accès administrateur et supprimer les comptes obsolètes ou inactifs.
*   **Surveillance et logs :** Mettre en place des alertes sur les connexions inhabituelles ou géographiquement suspectes (détection des accès via VPN).
*   **Protection des identifiants :** Imposer l'utilisation de coffres-forts de mots de passe sécurisés et limiter le stockage local d'identifiants sensibles sur des supports amovibles.

---
[Source](https://www.bleepingcomputer.com/news/security/ex-school-district-employee-jailed-for-hacks-on-former-employer/){:target="_blank"}
