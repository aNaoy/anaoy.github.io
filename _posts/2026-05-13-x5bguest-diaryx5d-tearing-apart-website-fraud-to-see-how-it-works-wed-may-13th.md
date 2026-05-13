---
title: '&#x5b;GUEST DIARY&#x5d; Tearing apart website fraud to see how it works., (Wed, May 13th)'
date: 2026-05-13
permalink: /posts/2026/05/13/x5bguest-diaryx5d-tearing-apart-website-fraud-to-see-how-it-works-wed-may-13th/
tags:
- veille-cyber
- sans-isc
---
### Anatomie des fraudes e-commerce : SEO poisoning et vol de données bancaires

Cette analyse met en lumière une campagne de fraude sophistiquée exploitant le « SEO poisoning » pour détourner des acheteurs vers de fausses places de marché. Les attaquants compromettent des sites légitimes (souvent WordPress) pour y injecter des sitemaps frauduleux, permettant à leurs produits fictifs de se classer dans les résultats de recherche Google.

**Points clés :**
* **Méthodologie :** Les escrocs volent des images et descriptions de produits réels (ex. eBay) pour donner une apparence de légitimité à leurs sites.
* **Technique de redirection :** Des sites web légitimes piratés servent de passerelles pour rediriger les victimes vers des plateformes de paiement malveillantes.
* **Processus de paiement :** Les sites utilisent des interfaces imitant Shopify ou PayPal pour capturer les informations de carte bancaire, avant de tenter des prélèvements multiples et non autorisés.
* **Automatisation :** L'usage d'outils d'IA permet aux attaquants de déployer massivement ces sites frauduleux en un temps record.

**Vulnérabilités exploitées :**
* **Compromission de sites tiers :** Utilisation de sites WordPress vulnérables (via des extensions malveillantes ou des identifiants compromis) pour héberger des contenus frauduleux.
* **Défaut de confiance en ligne :** La confiance des utilisateurs envers des sites apparaissant dans les résultats de recherche, malgré une création de domaine très récente (souvent quelques jours ou semaines).
* *Note : Aucune CVE spécifique n'est mentionnée, la menace reposant sur l'exploitation de configurations logicielles faibles ou de vecteurs d'attaque hybrides.*

**Recommandations :**
* **Vérification de la date de domaine :** Utiliser des outils WHOIS pour vérifier l'ancienneté d'un site. Un site marchand créé il y a quelques jours est suspect.
* **Analyse critique des prix :** Les offres « trop belles pour être vraies » doivent systématiquement alerter.
* **Recherche inversée d'images :** Effectuer une recherche inversée sur les photos des produits pour vérifier si elles ne sont pas copiées depuis des plateformes comme eBay ou Amazon.
* **Prudence lors des paiements :** Privilégier les cartes de paiement virtuelles à usage unique ou plafonnées (type Privacy.com) pour limiter le risque de prélèvements frauduleux récurrents.
* **Signalement :** Signaler les sites suspects aux services de cybersécurité et aux registrars de noms de domaine pour entraver l'infrastructure des attaquants.

---
[Source](https://isc.sans.edu/diary/rss/32958){:target="_blank"}
