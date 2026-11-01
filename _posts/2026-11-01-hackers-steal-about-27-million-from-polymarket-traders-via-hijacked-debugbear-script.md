---
title: 'Hackers Steal About $2.7 Million From Polymarket Traders via Hijacked DebugBear Script'
date: 2026-11-01
permalink: /posts/2026/11/01/hackers-steal-about-27-million-from-polymarket-traders-via-hijacked-debugbear-script/
tags:
- veille-cyber
- hackernews
---
### Vol de 2,7 millions de dollars sur Polymarket via un script tiers compromis

Le 29 octobre, la plateforme de prédictions Polymarket a été victime d'une attaque par injection de code malveillant, entraînant le vol d'environ 2,7 millions de dollars auprès de 726 utilisateurs. Le vecteur d'attaque était un script tiers fourni par **DebugBear**, un service de monitoring de performance web.

**Points clés :**
*   **Méthode d'attaque :** Les attaquants ont compromis les enregistrements DNS de DebugBear au niveau du registrar de domaine pour remplacer le script légitime par une version malveillante sur le site de Polymarket.
*   **Fonctionnement du script :** Le code injecté détournait les privilèges des utilisateurs connectés pour autoriser des transactions. Il interagissait directement avec le "signer" (validateur) du portefeuille de l'utilisateur pour transférer des fonds ou liquider des positions sans que l'utilisateur ne valide explicitement chaque action, contournant ainsi certaines protections classiques.
*   **Réponse de la plateforme :** Polymarket a rapidement suspendu ses services, supprimé le script, réinitialisé les sessions et remboursé l'intégralité des utilisateurs touchés (environ 3,9 millions de dollars au total, incluant les pertes connexes).

**Vulnérabilités exploitées :**
Il n'existe pas de CVE spécifique pour cette attaque, car elle repose sur une compromission de la chaîne d'approvisionnement logicielle (*Supply Chain Attack*). Les failles exploitées sont :
*   **Confiance excessive envers les scripts tiers :** Inclusion de code externe sans mécanismes de vérification d'intégrité.
*   **Absence de contrôle sur les ressources :** Manque de politiques de sécurité (Content Security Policy) strictes sur le chargement des scripts.

**Recommandations :**
*   **Pour les développeurs de sites :**
    *   Implémenter la **Subresource Integrity (SRI)** : cet attribut permet au navigateur de vérifier que le fichier chargé correspond à une empreinte numérique connue, empêchant l'exécution d'un fichier altéré.
    *   Renforcer la **Content Security Policy (CSP)** : restreindre strictement les domaines autorisés et les types d'actions autorisées.
    *   Minimiser l'utilisation de scripts tiers sur les pages sensibles (paiements, transactions).
*   **Pour les utilisateurs :**
    *   Toujours rejeter toute demande de signature de transaction non sollicitée ou inattendue sur un portefeuille crypto.

---
[Source](https://thehackernews.com/2026/11/hackers-steal-about-27-million-from.html){:target="_blank"}
