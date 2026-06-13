---
title: 'Maine disables data breach notification portal after fake disclosures'
date: 2026-06-13
permalink: /posts/2026/06/13/maine-disables-data-breach-notification-portal-after-fake-disclosures/
tags:
- veille-cyber
- bleepingcomp
---
### Désactivation du portail de notification des violations de données du Maine suite à des signalements frauduleux

Le bureau du procureur général du Maine a temporairement suspendu l'accès public à son portail de déclaration des violations de données. Cette décision fait suite à la publication de fausses notifications usurpant l'identité d'entreprises telles que Discord et VRChat.

**Points clés :**
*   **Abus du système :** Des tiers malveillants ont soumis de faux rapports de violations de données, lesquels étaient automatiquement publiés sur le site officiel sans vérification préalable.
*   **Impact :** Ces fausses déclarations, incluant des chiffres inventés (ex: 2,4 millions de personnes affectées pour VRChat), ont été utilisées pour diffuser de la désinformation et nuire à la réputation des entreprises concernées.
*   **Suspension :** Le portail est désormais inaccessible au public. Les entreprises peuvent toujours soumettre leurs déclarations, mais elles ne seront plus publiées automatiquement. Les demandes d'accès à ces données doivent désormais être traitées directement par le bureau du procureur.

**Vulnérabilités :**
*   **Absence de contrôle de validation :** Le processus reposait sur une publication automatique des données saisies, sans mécanisme d'authentification ou de vérification de la légitimité des soumissionnaires. (Note : Aucune CVE spécifique n'est associée, il s'agit d'une vulnérabilité de conception métier/processus).

**Recommandations :**
*   **Mise en place d'une validation humaine :** Introduire une étape de vérification administrative systématique avant toute publication publique des signalements reçus.
*   **Authentification forte :** Exiger une authentification vérifiée (via certificats ou comptes professionnels officiels) pour les entités soumettant des déclarations de violation.
*   **Révision des processus de publication :** Remplacer le système de publication automatique par un flux de travail validé pour garantir l'intégrité des informations diffusées sur les portails gouvernementaux.

---
[Source](https://www.bleepingcomputer.com/news/security/maine-disables-data-breach-notification-portal-after-fake-disclosures/){:target="_blank"}
