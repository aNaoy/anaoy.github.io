---
title: 'DoppelCart fraud network uses 119,000 fake shops to steal credit cards'
date: 2026-09-09
permalink: /posts/2026/09/09/doppelcart-fraud-network-uses-119000-fake-shops-to-steal-credit-cards/
tags:
- veille-cyber
- bleepingcomp
---
### DoppelCart : Un réseau massif de 119 000 boutiques frauduleuses

Le réseau « DoppelCart » représente actuellement la plus grande opération de sites e-commerce frauduleux jamais documentée. Utilisant plus de 119 000 domaines (principalement en .SHOP), ces sites usurpent l'identité de plus de 44 000 marques légitimes pour dérober des données bancaires.

**Points clés :**
*   **Ampleur :** Plus de 105 000 boutiques restent actives. Le réseau repose sur une structure automatisée partageant des fichiers de construction identiques et 27 backends de commerce.
*   **Mode opératoire :** Les sites imitent des marques réelles en copiant leurs catalogues et images. Ils attirent les victimes via des réductions fictives allant jusqu'à 65 %.
*   **Vol de données :** Le code de paiement capture en temps réel les numéros de carte, dates d'expiration, codes de sécurité, ainsi que les données personnelles (nom, adresse, email, téléphone).
*   **Contournement de sécurité :** Le script de paiement peut intercepter les codes de confirmation à usage unique (OTP) envoyés par les banques, permettant aux attaquants de valider des transactions frauduleuses.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'ingénierie sociale et le "skimming" de formulaires de paiement (web-skimming) plutôt que sur l'exploitation d'une faille logicielle dans le navigateur de la victime.

**Recommandations :**
*   **Pour les consommateurs :** Toujours vérifier l'URL du site avant tout achat, se méfier des remises anormalement élevées et privilégier les sites officiels connus.
*   **Pour les entreprises :**
    *   Surveiller activement le web pour détecter l'usurpation de marque et le "brand abuse".
    *   Utiliser des outils de veille, comme la base de données mise à disposition par Nebty, pour identifier si leur marque est utilisée par DoppelCart.
    *   Signaler les domaines contrefaits aux hébergeurs et aux autorités compétentes pour demander leur retrait.

---
[Source](https://www.bleepingcomputer.com/news/security/doppelcart-fraud-network-uses-119-000-fake-shops-to-steal-credit-cards/){:target="_blank"}
