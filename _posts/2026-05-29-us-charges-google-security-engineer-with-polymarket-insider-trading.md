---
title: 'US charges Google security engineer with Polymarket insider trading'
date: 2026-05-29
permalink: /posts/2026/05/29/us-charges-google-security-engineer-with-polymarket-insider-trading/
tags:
- veille-cyber
- bleepingcomp
---
### Délit d’initié chez Google : une exploitation interne sur Polymarket

Un ingénieur en sécurité de Google, Michele Spagnuolo, fait face à des poursuites judiciaires pour délit d’initié après avoir détourné des données confidentielles de l'entreprise pour réaliser 1,2 million de dollars de profits sur la plateforme de paris décentralisée Polymarket.

**Points clés :**
* **Le stratagème :** L'employé a utilisé son accès à un outil interne contenant les résultats confidentiels du classement « Year in Search » de Google.
* **L’exécution :** Sous le pseudonyme « AlphaRaccoon », il a parié avec une précision quasi parfaite sur des résultats de recherche spécifiques, misant un total de 2,75 millions de dollars.
* **Dissimulation :** Après que des spéculations sur les réseaux sociaux aient identifié une anomalie, l'ingénieur a tenté de masquer ses gains en faisant transiter les fonds via plusieurs services d'échange de cryptomonnaies visant à anonymiser les transactions.
* **Poursuites :** L'enquête du FBI et de la CFTC a permis de remonter jusqu'à lui grâce à ses documents d'identité. Il risque des peines cumulées pouvant atteindre plusieurs décennies de prison pour fraude, blanchiment d'argent et fraude aux matières premières.

**Vulnérabilités :**
* **Excès de privilèges :** Accès trop large accordé à un ingénieur sur des données commerciales hautement sensibles et non essentielles à ses fonctions techniques.
* **Absence de surveillance comportementale :** Incapacité des systèmes internes à détecter l'extraction massive ou l'utilisation anormale de données confidentielles par un utilisateur autorisé.
* **Pas de CVE applicable :** Il s'agit d'une faille liée à l'abus des droits d'accès (Insider Threat) plutôt qu'à une vulnérabilité logicielle spécifique.

**Recommandations :**
* **Gestion des accès (IAM) :** Appliquer strictement le principe du moindre privilège ; les accès aux données sensibles doivent être restreints aux seules personnes dont les missions le justifient réellement.
* **Audit et monitoring (DLP/UEBA) :** Déployer des outils de prévention contre la perte de données (DLP) et d'analyse comportementale (UEBA) pour détecter les téléchargements massifs ou l'utilisation suspecte d'informations confidentielles, même par des administrateurs.
* **Politiques de conformité :** Renforcer les politiques d'éthique et de transparence sur l'usage des données internes, avec des systèmes d'alerte automatique en cas d'accès inhabituel à des datasets sensibles ou marqués comme « confidentiels ».

---
[Source](https://www.bleepingcomputer.com/news/security/us-charges-google-security-engineer-with-polymarket-insider-trading/){:target="_blank"}
