---
title: 'How One Kubernetes YAML Can Hand Over a GCP Organization'
date: 2026-09-23
permalink: /posts/2026/09/23/how-one-kubernetes-yaml-can-hand-over-a-gcp-organization/
tags:
- veille-cyber
- bleepingcomp
---
### Risque d'élévation de privilèges via Google Kubernetes Config Connector

L'utilisation de **Google Kubernetes Config Connector (KCC)**, bien qu'efficace pour éliminer la prolifération des identifiants (secret sprawl) au sein d'une organisation, expose une vulnérabilité critique de type « **Confused Deputy** » (adjoint confus).

#### Points clés
*   **Fonctionnement :** KCC agit comme un contrôleur qui exécute des requêtes vers l'API Google Cloud avec ses propres privilèges, sans vérifier les droits du développeur ayant soumis la configuration YAML.
*   **La faille :** Si un attaquant dispose de droits d'écriture sur des ressources `IAMPolicyMember` au sein d'un espace de noms (namespace) surveillé par KCC, il peut ordonner à celui-ci de modifier des politiques IAM à l'échelle de l'organisation.
*   **Conséquence :** Un utilisateur sans aucune autorisation cloud peut élever ses privilèges jusqu'à devenir « Owner » (propriétaire) de l'organisation GCP, en exploitant simplement les permissions trop larges accordées au service account de KCC.

#### Vulnérabilités
*   **ConfigConfusion :** Il ne s'agit pas d'un bug logiciel classique avec un identifiant CVE, mais d'une faille de conception liée à l'absence de vérification croisée entre l'identité Kubernetes et l'identité Google Cloud. La séparation entre le contrôle d'accès RBAC (Kubernetes) et l'IAM (Google Cloud) permet aux attaquants d'outrepasser les restrictions de sécurité.

#### Recommandations
Pour sécuriser votre instance KCC, il est impératif de restreindre ses privilèges :

*   **Segmentation par Namespace :** Adoptez le mode « namespaced » en utilisant des comptes de service Google dédiés et restreints pour chaque espace de noms, plutôt qu'un compte unique pour toute l'organisation.
*   **Principe du moindre privilège :** Auditez et réduisez les rôles IAM du compte de service KCC. Évitez absolument les rôles `roles/owner` ou `roles/resourcemanager.organizationAdmin` si ce n'est pas strictement indispensable.
*   **Contrôle d'accès Kubernetes :** Limitez strictement la capacité à créer ou modifier des ressources `IAMPolicyMember`, `IAMPolicy` et `IAMPartialPolicy` aux seules équipes d'infrastructure ou aux administrateurs de plateforme via Kubernetes RBAC.
*   **Surveillance :** Mettez en place un monitoring actif sur les modifications IAM effectuées par KCC, particulièrement celles qui impactent les dossiers ou l'organisation, afin de détecter toute exécution hors des workflows GitOps approuvés.

---
[Source](https://www.bleepingcomputer.com/news/security/how-one-kubernetes-yaml-can-hand-over-a-gcp-organization/){:target="_blank"}
