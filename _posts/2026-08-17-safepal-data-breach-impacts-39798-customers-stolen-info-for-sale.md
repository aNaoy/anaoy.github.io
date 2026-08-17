---
title: 'SafePal data breach impacts 39,798 customers, stolen info for sale'
date: 2026-08-17
permalink: /posts/2026/08/17/safepal-data-breach-impacts-39798-customers-stolen-info-for-sale/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données chez SafePal : 39 798 clients exposés

Le fournisseur de portefeuilles matériels de cryptomonnaies SafePal a subi une fuite de données affectant 39 798 clients ayant passé commande entre mars 2025 et avril 2026. Les informations dérobées sont actuellement mises en vente sur un forum cybercriminel.

**Points clés :**
*   **Données exposées :** Noms, adresses e-mail, adresses de livraison, numéros de téléphone et détails des achats.
*   **Données sécurisées :** Les phrases de récupération (seed phrases), clés privées, mots de passe et données bancaires n'ont pas été compromis.
*   **Vecteur d'attaque :** Une faille d'autorisation dans le module de suivi de commande d'un plug-in tiers a permis un accès non autorisé aux informations. Une erreur de configuration a également empêché la suppression automatique des données, facilitant la collecte massive.
*   **Risques :** Les données volées sont utilisées pour des campagnes de phishing ciblé et des tentatives d'ingénierie sociale (ex: faux appels au support, demandes de mise à jour de firmware).

**Vulnérabilités :**
*   Faille d'autorisation dans la fonction de suivi de commande (Plug-in).
*   Défaut de configuration (Data-cleanup process) ayant entraîné une rétention illégale de données personnelles.
*   *(Note : Aucune CVE spécifique n'a été attribuée à ces vulnérabilités logicielles internes.)*

**Recommandations :**
*   **Vérification :** Utiliser l'outil de vérification officiel sur le site de SafePal pour confirmer si vos données sont concernées.
*   **Vigilance accrue :** Se méfier de tout e-mail ou appel téléphonique concernant des mises à jour de firmware, des retours produits ou des enquêtes, particulièrement s'ils incitent à divulguer des clés privées ou des seed phrases.
*   **Action immédiate en cas de compromission :** Si vous avez déjà divulgué votre phrase de récupération, transférez immédiatement vos fonds vers un nouveau portefeuille sécurisé.
*   **Sécurité des actifs :** Aucun remplacement de matériel n'est requis si les clés privées n'ont pas été partagées avec des tiers.

---
[Source](https://www.bleepingcomputer.com/news/security/safepal-data-breach-impacts-39-798-customers-stolen-info-for-sale/){:target="_blank"}
