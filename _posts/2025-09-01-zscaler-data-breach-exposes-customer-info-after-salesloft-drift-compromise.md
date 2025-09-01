---
title: 'Zscaler data breach exposes customer info after Salesloft Drift compromise'
date: 2025-09-01
permalink: /posts/2025/09/01/zscaler-data-breach-exposes-customer-info-after-salesloft-drift-compromise/
tags:
- veille-cyber
- bleepingcomp
---
## Compromission de la chaîne d'approvisionnement : Informations client Zscaler exposées

La société de cybersécurité Zscaler a subi une violation de données après que des acteurs malveillants aient accédé à son instance Salesforce via une compromission de Salesloft Drift, un agent de chat IA intégré à Salesforce. Cet accès a permis aux attaquants de voler des informations client, notamment des noms, des adresses e-mail professionnelles, des titres de poste, des numéros de téléphone, des détails de localisation, des informations de licence produit et des données de cas de support.

L'incident s'inscrit dans une campagne plus large ciblant les instances Salesforce par le biais d'attaques de chaîne d'approvisionnement, utilisant souvent le phishing vocal (vishing) pour inciter les employés à lier des applications OAuth malveillantes. Le groupe de menaces UNC6395 est identifié comme étant derrière ces attaques, qui ont également exploité des jetons OAuth volés pour accéder aux comptes de messagerie Google Workspace.

**Points Clés :**

*   **Attaque de chaîne d'approvisionnement :** La compromission initiale de Salesloft Drift a permis aux attaquants d'accéder aux données de ses clients, dont Zscaler.
*   **Exposition des données client :** Des informations personnelles et professionnelles relatives aux clients de Zscaler ont été exfiltrées.
*   **Aucun impact sur les produits Zscaler :** Zscaler affirme que seuls ses systèmes Salesforce ont été affectés, et non ses produits, services ou infrastructure principaux.
*   **Vigilance accrue :** La société recommande aux clients de rester attentifs aux tentatives de phishing et d'ingénierie sociale.
*   **Mesures correctives :** Zscaler a révoqué les intégrations Salesloft Drift, fait pivoter d'autres jetons API et renforcé ses protocoles d'authentification pour les appels de support.
*   **Contexte plus large :** Cet incident fait partie d'une série de violations de données affectant diverses entreprises via des attaques similaires sur la plateforme Salesforce.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifiques. La vulnérabilité principale réside dans la **compromission de la chaîne d'approvisionnement** par l'exploitation de l'intégration Salesloft Drift, permettant le vol de **jetons OAuth et de rafraîchissement**. Cela a conduit à un accès non autorisé aux données sensibles.

**Recommandations :**

*   Les clients doivent rester **vigilants contre les attaques de phishing et d'ingénierie sociale** qui pourraient exploiter les informations exposées.
*   Zscaler a révoqué toutes les intégrations Salesloft Drift, fait pivoter d'autres jetons API et renforcé son protocole d'authentification pour les appels de support.

---
[Source](https://www.bleepingcomputer.com/news/security/zscaler-data-breach-exposes-customer-info-after-salesloft-drift-compromise/){:target="_blank"}
