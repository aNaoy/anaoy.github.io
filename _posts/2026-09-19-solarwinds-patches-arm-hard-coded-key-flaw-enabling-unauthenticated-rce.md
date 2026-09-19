---
title: 'SolarWinds Patches ARM Hard-Coded Key Flaw Enabling Unauthenticated RCE'
date: 2026-09-19
permalink: /posts/2026/09/19/solarwinds-patches-arm-hard-coded-key-flaw-enabling-unauthenticated-rce/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans SolarWinds Access Rights Manager

SolarWinds a publié des correctifs pour corriger une vulnérabilité critique affectant **Access Rights Manager (ARM)**, permettant à un attaquant non authentifié d'exécuter du code à distance. Cette faille, découverte par le chercheur Kai Huang, est causée par l'utilisation d'une clé statique codée en dur dans le logiciel.

**Points clés :**
*   **Vulnérabilité principale :** Exécution de code à distance (RCE) non authentifiée via une clé codée en dur.
*   **CVE associée :** [CVE-2026-28326](https://www.solarwinds.com/trust-center/security-advisories/cve-2026-28326) (Score CVSS : 8.8).
*   **Produits impactés :** Toutes les versions d'Access Rights Manager jusqu'à la version 2026.2 incluse.
*   **État de l'exploitation :** Aucune preuve d'exploitation active dans la nature n'a été signalée à ce jour.
*   **Autres correctifs :** SolarWinds a également récemment corrigé plusieurs vulnérabilités critiques dans *Web Help Desk* (bypass d'authentification SAML, DoS) et *Serv-U* (élévation de privilèges, RCE).

**Recommandations :**
*   Mettre immédiatement à jour SolarWinds Access Rights Manager vers la version **2026.2.1** ou ultérieure.
*   Appliquer les correctifs pour les autres produits SolarWinds (Web Help Desk et Serv-U) si ces solutions sont déployées au sein de votre infrastructure, afin de prévenir les risques d'élévation de privilèges et de contournement d'authentification.

---
[Source](https://thehackernews.com/2026/09/solarwinds-patches-arm-hard-coded-key.html){:target="_blank"}
