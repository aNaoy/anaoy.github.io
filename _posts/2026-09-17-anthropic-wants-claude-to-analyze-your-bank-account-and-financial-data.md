---
title: 'Anthropic wants Claude to analyze your bank account and financial data'
date: 2026-09-17
permalink: /posts/2026/09/17/anthropic-wants-claude-to-analyze-your-bank-account-and-financial-data/
tags:
- veille-cyber
- bleepingcomp
---
### L'intégration des données bancaires dans Claude : Enjeux et risques

Anthropic teste actuellement une nouvelle fonctionnalité nommée « Claude Money » au sein de son application iOS, permettant aux utilisateurs de connecter directement leurs comptes bancaires pour analyser leurs dépenses, leurs investissements et leur situation financière. Ce service s'inscrit dans une tendance similaire à celle déjà proposée par OpenAI avec Plaid.

**Points clés :**
* **Fonctionnalité :** Intégration directe des données financières personnelles dans l'interface de l'IA pour obtenir des insights budgétaires.
* **Disponibilité :** Phase de test très limitée, sans détails sur les institutions bancaires supportées ou la zone géographique visée.
* **Comparaison :** Le modèle de fonctionnement ressemble fortement à celui de ChatGPT, qui s'appuie sur des services tiers (comme Plaid) pour agréger les données financières.

**Risques et vulnérabilités :**
* **Risque de confidentialité :** L'exposition de données bancaires hautement sensibles à des modèles d'IA accroît la surface d'attaque en cas de compromission des comptes ou des jetons d'accès API.
* **Conformité réglementaire :** Les strictes législations européennes sur la protection des données (RGPD) pourraient restreindre, voire empêcher le déploiement de cette fonctionnalité en Europe.
* **Vulnérabilités logicielles :** Bien qu'aucune CVE spécifique ne soit liée à cette annonce, l'intégration de services tiers (API bancaires) introduit une dépendance sécuritaire supplémentaire où une faille dans le service d'agrégation pourrait compromettre l'ensemble des données financières des utilisateurs.

**Recommandations :**
* **Principe de moindre privilège :** Éviter de connecter des comptes bancaires principaux comportant des économies importantes à des services d'IA en phase expérimentale.
* **Vérification des permissions :** Analyser scrupuleusement les accès accordés aux tiers (OAuth) et révoquer les accès inutilisés.
* **Surveillance active :** Surveiller les annonces officielles d'Anthropic concernant les politiques de confidentialité, notamment sur l'utilisation des données pour le réentraînement des modèles, afin de garantir que vos informations financières restent strictement privées.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/anthropic-wants-claude-to-analyze-your-bank-account-and-financial-data/){:target="_blank"}
