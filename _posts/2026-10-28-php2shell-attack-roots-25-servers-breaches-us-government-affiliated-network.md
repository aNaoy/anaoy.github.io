---
title: 'PHP2Shell Attack Roots 25 Servers, Breaches U.S. Government-Affiliated Network'
date: 2026-10-28
permalink: /posts/2026/10/28/php2shell-attack-roots-25-servers-breaches-us-government-affiliated-network/
tags:
- veille-cyber
- hackernews
---
### Compromission de serveurs gouvernementaux via PHP2Shell et l'IA

Un acteur étatique présumé, d'origine chinoise, a mené une campagne d'attaques sophistiquées en utilisant des outils assistés par IA pour compromettre 25 serveurs, dont trois au sein d'une infrastructure affiliée au gouvernement américain. Cette opération illustre la dangerosité de l'exposition des interfaces de gestion de pare-feu sur Internet.

**Points clés :**
*   **Mode opératoire :** L'attaquant a utilisé le moteur de recherche FOFA pour identifier 19 000 pare-feu exposés, puis a automatisé le ciblage de systèmes spécifiques (PHP 8.0.30) via un script personnalisé.
*   **Assistance par IA :** L'infrastructure d'attaque intégrait des outils tels que *Claude Code* et des plateformes comme *aiscan* (utilisant DeepSeek et Kimi) pour le développement et l'optimisation des scripts d'exploitation.
*   **Objectif final :** Après l'accès initial, l'attaquant a ciblé l'Active Directory via des tunnels SSH inversés pour tenter d'extraire des identifiants, énumérer des utilisateurs et créer des comptes dérobés.

**Vulnérabilités exploitées :**
*   **PHP2Shell (CVE-2026-109618 et CVE-2026-109619) :** Score CVSS 9.2, permettant l'exécution de code à distance (RCE) via le mécanisme `session.upload_progress`.
*   **Fragnesia (CVE-2026-46300) :** Score CVSS 7.8, vulnérabilité d'élévation de privilèges locale (LPE) au niveau du noyau Linux, utilisée pour obtenir les droits root sur les systèmes cibles.

**Recommandations :**
*   **Réduction de la surface d'attaque :** Limiter strictement l'accès aux interfaces de gestion des pare-feu en les isolant du réseau public.
*   **Mise à jour et durcissement :** Appliquer immédiatement les correctifs pour PHP et le noyau Linux. Pour les environnements utilisant PHP 8.0.30, une vigilance accrue est nécessaire sur la configuration des limites de mémoire.
*   **Surveillance Active Directory :** Auditer les logs pour détecter des comportements anormaux, tels que des tentatives de pulvérisation de mots de passe (*password spraying*) ou la création de comptes suspects.
*   **Détection de tunnels persistants :** Rechercher les connexions SSH sortantes inhabituelles provenant des équipements de périmètre vers des infrastructures inconnues.

---
[Source](https://thehackernews.com/2026/10/php2shell-attack-roots-25-servers.html){:target="_blank"}
