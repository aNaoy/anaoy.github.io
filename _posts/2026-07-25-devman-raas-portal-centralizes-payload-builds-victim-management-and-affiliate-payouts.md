---
title: 'DevMan RaaS Portal Centralizes Payload Builds, Victim Management, and Affiliate Payouts'
date: 2026-07-25
permalink: /posts/2026/07/25/devman-raas-portal-centralizes-payload-builds-victim-management-and-affiliate-payouts/
tags:
- veille-cyber
- hackernews
---
### Le portail DevMan : Industrialisation du RaaS et cyber-extorsion

Le groupe de ransomware **DevMan** (traqué sous le nom de *Funky Mantis*) a professionnalisé ses opérations grâce à une plateforme de Ransomware-as-a-Service (RaaS) centralisée. Ce portail permet aux affiliés de générer des payloads, de gérer les victimes, de suivre les paiements et d'orchestrer les attaques de manière structurée.

**Points clés :**
*   **Structuration hiérarchique :** L'organisation repose sur des rôles définis (administrateurs, coordinateurs d'accès, opérateurs seniors et affiliés), avec un système de parrainage et de probation pour les nouveaux venus.
*   **Capacités techniques :** DevMan cible les infrastructures critiques et a développé un locker spécialisé pour les systèmes SCADA, visant à provoquer des dommages physiques par surchauffe matérielle.
*   **Modèle économique :** Le partage des gains est fixé à 80 % pour l'affilié et 20 % pour l'administration.
*   **Évolution de la menace :** La version 3 du portail, lancée en janvier 2026, automatise le cycle de vie complet des intrusions, réduisant l'autonomie des affiliés pour garantir un meilleur contrôle opérationnel.
*   **Controverse interne :** Une enquête interne chez la firme de cybersécurité Huntress a révélé qu'une analyste a transmis des communications confidentielles du FBI au groupe DevMan, qualifiant cet acte de "manque de jugement", bien que critiqué comme une menace interne par d'anciens employés.

**Vulnérabilités et capacités d'attaque :**
*   **Logiciel malveillant :** Le chiffrement utilise l'algorithme **ChaCha20-Poly1305**.
*   **Méthodes :** Privilège d'élévation, terminaison de processus/services critiques, suppression des journaux d'événements, mouvement latéral et chiffrement multi-threadé.
*   **CVE :** Aucune CVE spécifique mentionnée, l'attaque repose sur l'abus d'accès distants (VPN/LDAP) et le vol d'identifiants privilégiés.

**Recommandations :**
*   **Gestion des accès :** Prohiber l'utilisation des comptes de service et de sauvegarde pour des connexions VPN interactives, sauf nécessité opérationnelle stricte.
*   **Authentification :** Généraliser l'usage d'une authentification multifacteur (MFA) résistante au phishing pour tous les accès distants et l'administration privilégiée.
*   **Hygiène des identifiants :** Procéder à une rotation régulière des secrets (identifiants, jetons) exposés dans les appliances VPN, intégrations LDAP, scripts d'automatisation et outils de sauvegarde.
*   **Surveillance :** Prioriser la protection et la surveillance des comptes possédant des droits d'administration locale ou de domaine.

---
[Source](https://thehackernews.com/2026/07/devman-raas-portal-centralizes-payload.html){:target="_blank"}
