---
title: 'Palo Alto Networks data breach exposes customer info, support cases'
date: 2025-09-02
permalink: /posts/2025/09/02/palo-alto-networks-data-breach-exposes-customer-info-support-cases/
tags:
- veille-cyber
- bleepingcomp
---
**Vol de données chez Palo Alto Networks : Impact d'une attaque par chaîne d'approvisionnement sur les informations clients**

Palo Alto Networks a été victime d'une violation de données suite à l'exploitation de jetons OAuth compromis lors d'une attaque sur Salesloft. Cette faille a permis à des acteurs malveillants d'accéder à l'instance Salesforce de l'entreprise, exposant ainsi des informations clients et des données de cas de support.

**Points Clés :**

*   L'incident est lié à une attaque par chaîne d'approvisionnement plus large ciblant l'application Salesloft Drift.
*   Les attaquants ont utilisé des jetons OAuth volés pour accéder aux données de Salesforce.
*   Les informations compromises incluent principalement des informations de contact commercial, des enregistrements de comptes de vente et des données de cas de support de base (sans fichiers techniques ni pièces jointes).
*   Les attaquants ont recherché des secrets tels que des clés d'accès AWS, des jetons Snowflake, des informations d'identification VPN et SSO, ainsi que des mots tels que "password", "secret" ou "key" pour faciliter des attaques ultérieures.
*   Les méthodes d'attaque comprenaient l'utilisation d'outils Python personnalisés, la suppression de journaux pour masquer les traces et l'utilisation de Tor pour l'anonymisation.

**Vulnérabilités :**

*   Compromission de jetons OAuth via l'attaque sur Salesloft Drift.
*   Vulnérabilités d'accès aux données sensibles au sein de l'instance Salesforce de Palo Alto Networks.

**Recommandations :**

*   **Pour les clients de Salesloft Drift :**
    *   Investiguer les journaux Salesforce, d'identité et réseau.
    *   Examiner toutes les intégrations Drift pour des connexions suspectes.
    *   Révoquer et rotationner les clés d'authentification, les identifiants et les secrets.
    *   Utiliser des outils automatisés (comme Trufflehog, Gitleaks) pour scanner les dépôts de code à la recherche de clés ou de jetons intégrés.
    *   Vérifier les données exfiltrées pour la présence d'identifiants si une fuite est confirmée.
*   **Actions de Palo Alto Networks :**
    *   Révocation des jetons associés et rotation des identifiants.
    *   Désactivation des intégrations Drift dans leur environnement Salesforce.
    *   Notification directe aux clients impactés.

---
[Source](https://www.bleepingcomputer.com/news/security/palo-alto-networks-data-breach-exposes-customer-info-support-cases/){:target="_blank"}
