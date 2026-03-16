---
title: 'UK’s Companies House confirms security flaw exposed business data'
date: 2026-03-16
permalink: /posts/2026/03/16/uks-companies-house-confirms-security-flaw-exposed-business-data/
tags:
- veille-cyber
- bleepingcomp
---
### Faille de sécurité critique chez Companies House : Données d'entreprises exposées

Le service « WebFiling » de l'agence gouvernementale britannique Companies House a été suspendu après la découverte d'une vulnérabilité majeure active depuis octobre 2025. Cette faille a permis, pendant cinq mois, l'exposition des données sensibles de cinq millions d'entreprises.

**Points clés :**
* **Origine du problème :** Une mise à jour du système WebFiling effectuée en octobre 2025 a introduit une erreur de logique dans la gestion des sessions utilisateur.
* **Méthode d'exploitation :** En tentant d'accéder au dossier d'une autre entreprise via le portail, un utilisateur authentifié pouvait contourner la demande de code d'authentification en revenant simplement sur la page précédente, accédant ainsi illégalement au tableau de bord tiers.
* **Impact des données :** Exposition d'informations privées telles que des adresses personnelles, des adresses e-mail et des dates de naissance.
* **Risque d'intégrité :** La faille permettait également d'effectuer des modifications non autorisées sur les dossiers des entreprises (changement de directeur, dépôts de comptes, etc.).
* **Ce qui est épargné :** Aucun mot de passe, aucune donnée de vérification d'identité (passeports) et aucun document déjà archivé n'ont été compromis ou altérés.

**Vulnérabilités :**
* Aucune CVE n'a été assignée à ce jour pour cet incident spécifique, le problème étant lié à une erreur de logique applicative côté serveur lors de la gestion des accès par les utilisateurs authentifiés.

**Recommandations :**
* **Pour l'organisme :** Mener une enquête approfondie pour identifier si la faille a été exploitée de manière malveillante et notifier les entités dont les données ont été potentiellement consultées ou modifiées. Une mise en conformité avec les autorités compétentes (ICO et NCSC) est déjà en cours.
* **Pour les entreprises :** Vérifier l'historique des modifications récentes apportées à leurs dossiers sur le portail Companies House afin de détecter toute activité suspecte ou enregistrement non autorisé effectué depuis octobre 2025.

---
[Source](https://www.bleepingcomputer.com/news/security/uks-companies-house-confirms-security-flaw-exposed-business-data/){:target="_blank"}
