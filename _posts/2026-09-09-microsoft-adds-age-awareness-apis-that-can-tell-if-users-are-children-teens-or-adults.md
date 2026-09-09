---
title: 'Microsoft adds age-awareness APIs that can tell if users are children, teens, or adults'
date: 2026-09-09
permalink: /posts/2026/09/09/microsoft-adds-age-awareness-apis-that-can-tell-if-users-are-children-teens-or-adults/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation des expériences numériques via les nouvelles API d'âge de Windows 11

Microsoft introduit de nouvelles API d'âge dans Windows 11 permettant aux applications de déterminer la tranche d'âge d'un utilisateur (moins de 10 ans, 10-12, 13-15, 16-17, 18+) sans accéder à sa date de naissance complète. Ce mécanisme s'appuie sur le système *Microsoft Age Verification* (MAV) pour renforcer la sécurité et la conformité des contenus, notamment pour les services d'IA.

**Points clés :**
* **Protection de la vie privée :** Les développeurs reçoivent uniquement un signal de catégorie d'âge via les fonctions `GetUserAgeRangeAsync` et `GetAgeVerificationStatusAsync`, minimisant ainsi la collecte de données personnelles.
* **Vérification centralisée :** Le concept « vérifier une fois, utiliser partout » permet aux applications de consulter le statut de vérification validé par Microsoft, évitant les demandes répétées de preuve d'âge.
* **Contrôle parental :** Ces API facilitent l'ajustement automatique des restrictions et protections adaptées aux mineurs, renforçant les outils de contrôle parental lors de la configuration de Windows.
* **Déploiement :** La fonctionnalité est actuellement disponible pour les Windows Insiders et sera bientôt généralisée.

**Vulnérabilités :**
* Aucune vulnérabilité CVE n'est associée à cette mise à jour. Il s'agit d'une évolution fonctionnelle visant à renforcer la conformité réglementaire et la protection des mineurs.

**Recommandations :**
* **Développeurs :** Intégrer ces API pour automatiser la mise en conformité des applications (restrictions de contenu, protection des données) vis-à-vis des différents segments d'âge, conformément aux exigences réglementaires croissantes.
* **Utilisateurs :** Maintenir les paramètres de contrôle parental à jour lors de la configuration initiale de Windows pour garantir l'application efficace des protections sur les comptes mineurs.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-adds-age-awareness-apis-that-can-tell-if-users-are-children-teens-or-adults/){:target="_blank"}
