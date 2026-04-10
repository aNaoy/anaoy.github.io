---
title: 'Google rolls out Gmail end-to-end encryption on mobile devices'
date: 2026-04-10
permalink: /posts/2026/04/10/google-rolls-out-gmail-end-to-end-encryption-on-mobile-devices/
tags:
- veille-cyber
- bleepingcomp
---
### Déploiement du chiffrement de bout en bout sur l'application mobile Gmail

Google étend le chiffrement de bout en bout (E2EE) à l'application Gmail sur Android et iOS pour les utilisateurs professionnels. Cette fonctionnalité permet de rédiger et de lire des courriels chiffrés nativement sans nécessiter d'outils tiers, garantissant que les données restent inaccessibles aux serveurs de Google et aux tiers.

**Points clés :**
* **Compatibilité élargie :** Les messages peuvent être envoyés à n'importe quel destinataire, y compris ceux n'utilisant pas Gmail (lecture via un navigateur web).
* **Technologie utilisée :** Le chiffrement côté client (CSE) permet aux organisations de gérer leurs propres clés de chiffrement en dehors des serveurs de Google.
* **Accessibilité :** Disponible pour les abonnés Google Workspace avec licence *Enterprise Plus* et modules complémentaires *Assured Controls*.

**Vulnérabilités :**
* Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article. La mise en œuvre du chiffrement côté client vise précisément à réduire la surface d'exposition aux menaces liées au traitement des données sur le cloud.

**Recommandations :**
* **Activation administrative :** Les administrateurs doivent activer manuellement les clients Android et iOS via la console d'administration Google Workspace sous l'interface de gestion du chiffrement côté client (CSE).
* **Usage utilisateur :** Pour sécuriser un message, les utilisateurs doivent activer l'option « Chiffrement supplémentaire » en cliquant sur l'icône de cadenas lors de la rédaction d'un courriel.
* **Conformité :** Utiliser cette fonctionnalité pour répondre aux exigences de souveraineté des données, aux normes HIPAA et aux contrôles d'exportation.

---
[Source](https://www.bleepingcomputer.com/news/google/google-rolls-out-gmail-end-to-end-encryption-on-mobile-devices/){:target="_blank"}
