---
title: 'Former govt contractor convicted for wiping dozens of federal databases'
date: 2026-05-08
permalink: /posts/2026/05/08/former-govt-contractor-convicted-for-wiping-dozens-of-federal-databases/
tags:
- veille-cyber
- bleepingcomp
---
### Sabotage informatique : Condamnation pour destruction de données fédérales

Sohaib Akhter, un entrepreneur fédéral, a été reconnu coupable d'avoir délibérément supprimé environ 96 bases de données gouvernementales sensibles en février 2025. Suite à leur licenciement immédiat après la découverte de leurs antécédents criminels (une condamnation antérieure pour accès non autorisé aux systèmes du département d'État), Akhter et son frère Muneeb ont lancé une attaque par vengeance contre leur ancien employeur.

**Points clés :**
* **Motivation :** Acte de représailles suite à une rupture de contrat de travail.
* **Impact :** Suppression massive de documents d'enquête fédérale et de dossiers liés au *Freedom of Information Act*.
* **Obstruction :** Les individus ont activement cherché à effacer les journaux système (logs) — utilisant notamment une IA pour obtenir des instructions techniques — et ont tenté de détruire des preuves physiques (laptops) avant l'intervention des autorités.
* **Conséquences judiciaires :** Sohaib Akhter encourt jusqu'à 21 ans de prison, tandis que son frère Muneeb encourt jusqu'à 45 ans pour des chefs d'accusation incluant fraude informatique et vol d'identité aggravé.

**Vulnérabilités exploitées :**
* **Gestion des privilèges (IAM) :** Maintien d'accès réseau ou accès distant non révoqué immédiatement au moment du licenciement.
* **Absence de protection contre la manipulation de logs :** Les systèmes n'étaient pas suffisamment sécurisés contre l'effacement des traces d'activité par des utilisateurs internes (insider threat).
* *Note : Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'un abus de privilèges d'accès légitimes plutôt que de l'exploitation d'une vulnérabilité logicielle.*

**Recommandations :**
* **Révoquer les accès en temps réel :** Automatiser la désactivation immédiate de tous les accès (VPN, comptes cloud, bases de données) lors de la notification de licenciement.
* **Immuabilité des logs :** Centraliser les journaux d'audit sur des serveurs sécurisés et distants, configurés en mode "écriture seule" (WORM - Write Once, Read Many), afin d'empêcher tout administrateur ou utilisateur de les supprimer après un acte malveillant.
* **Segmentation et restriction :** Appliquer strictement le principe du moindre privilège, limitant la capacité d'un utilisateur à supprimer des bases de données entières, même si ses accès n'ont pas encore été révoqués.
* **Vérification des antécédents :** Renforcer les protocoles de vérification des antécédents pour les contractuels ayant accès à des infrastructures critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/former-govt-contractor-convicted-for-wiping-dozens-of-federal-databases/){:target="_blank"}
