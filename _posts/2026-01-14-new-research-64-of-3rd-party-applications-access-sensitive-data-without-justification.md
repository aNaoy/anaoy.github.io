---
title: 'New Research: 64% of 3rd-Party Applications Access Sensitive Data Without Justification'
date: 2026-01-14
permalink: /posts/2026/01/14/new-research-64-of-3rd-party-applications-access-sensitive-data-without-justification/
tags:
- veille-cyber
- hackernews
---
**Risque Accru des Applications Tierces : Accès Non Justifié aux Données Sensibles**

Une étude récente portant sur 4 700 sites web de premier plan révèle une augmentation alarmante de 64 % des applications tierces accédant à des données sensibles sans justification commerciale valable, un chiffre en hausse par rapport aux 51 % de l'année précédente. Ce phénomène touche particulièrement les secteurs gouvernemental, où l'activité malveillante a bondi de 2 % à 12,9 %, et éducatif, avec un site sur sept présentant des signes de compromission active.

**Points Clés :**

*   **Augmentation de l'accès non justifié :** 64 % des applications tierces accèdent à des données sensibles sans besoin métier prouvé.
*   **Secteurs visés :** Le secteur gouvernemental a vu une augmentation significative de l'activité malveillante (12,9 %), et un site éducatif sur sept est compromis.
*   **Principaux acteurs :** Google Tag Manager (8 %), Shopify (5 %) et Facebook Pixel (4 %) sont identifiés comme des contributeurs majeurs à ce risque.
*   **Désalignement entre priorité et action :** Bien que 81 % des responsables de la sécurité considèrent les cyberattaques web comme une priorité, seulement 39 % ont mis en place des solutions pour y remédier.
*   **Cause fondamentale :** Un manque de gouvernance, où les équipes marketing déploient des applications sans supervision adéquate de l'IT, entraînant des sur-permissions.
*   **Marketing vs. IT :** Les départements marketing sont responsables de 43 % du risque d'exposition des tiers, contre 19 % pour l'IT.

**Vulnérabilités Identifiées :**

Les vulnérabilités proviennent principalement d'un accès accordé sans justification métier appropriée, caractérisé par :

*   **Fonctionnalité non pertinente :** Lecture de données inutiles à la tâche de l'application (ex: un chatbot accédant aux informations de paiement).
*   **Présence sans retour sur investissement (ROI) :** Applications actives sur des pages à haut risque sans transmission de données pendant plus de 90 jours.
*   **Déploiement caché :** Injection via des gestionnaires de balises sans supervision de sécurité ou respect du principe de moindre privilège.
*   **Sur-permissions :** Utilisation d'un accès "Full DOM Access" (accès complet au DOM) pour collecter des pages entières au lieu d'éléments restreints.
*   **Impact potentiel :** Un incident lié au pixel Facebook, utilisé par 53,2 % des sites, pourrait avoir un impact 5 fois supérieur à celui de l'attaque Polyfill.io, affectant potentiellement plus de 2,5 millions de sites instantanément.

Aucune vulnérabilité spécifique avec un identifiant CVE n'est explicitement mentionnée dans l'article pour ces applications tierces dans le contexte de l'accès non justifié. Cependant, les descriptions des vulnérabilités listées ci-dessus correspondent à des failles de sécurité logique et de configuration.

**Recommandations :**

1.  **Audit des traqueurs :** Inventorier chaque pixel et traqueur, identifier le propriétaire et la justification métier, et supprimer les outils ne pouvant justifier l'accès aux données.
    *   **Corrections prioritaires :** Désactiver "Automatic Advanced Matching" du Facebook Pixel sur les pages contenant des informations personnelles identifiables (PII) ; vérifier que Google Tag Manager n'accède pas aux pages de paiement ; examiner les permissions des applications Shopify.
2.  **Mise en œuvre de la surveillance automatisée :** Déployer une surveillance en temps réel pour détecter l'accès aux champs sensibles (cartes de crédit, numéros de sécurité sociale, identifiants), les alertes pour la collecte non autorisée et le suivi des violations de politique de sécurité (CSP).
3.  **Résolution du fossé Marketing-IT :** Organiser des revues conjointes entre le CISO et le CMO concernant les outils marketing dans les cadres de paiement, le périmètre d'application du Facebook Pixel (utilisation de listes d'autorisation/exclusion) et l'évaluation du ROI des traqueurs par rapport aux risques de sécurité.
4.  **Mise en place de la gestion de l'exposition web :** Adopter une approche de gestion de l'exposition web (Web Exposure Management) pour sécuriser les risques liés aux applications tierces.
5.  **Application du principe de moindre privilège :** S'assurer que les applications tierces n'obtiennent que les permissions strictement nécessaires à leur fonctionnement.

---
[Source](https://thehackernews.com/2026/01/new-research-64-of-3rd-party.html){:target="_blank"}
