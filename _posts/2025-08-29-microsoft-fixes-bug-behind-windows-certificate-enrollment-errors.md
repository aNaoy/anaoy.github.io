---
title: 'Microsoft fixes bug behind Windows certificate enrollment errors'
date: 2025-08-29
permalink: /posts/2025/08/29/microsoft-fixes-bug-behind-windows-certificate-enrollment-errors/
tags:
- veille-cyber
- bleepingcomp
---
**Correction des erreurs de certificat dans Windows 11**

Microsoft a résolu un problème qui générait de faux messages d'erreur liés au 'Microsoft Pluton Cryptographic Provider' dans le composant CertificateServicesClient (CertEnroll) suite à l'installation des mises à jour de juillet 2025 et des versions ultérieures de Windows 11 24H2. Ces erreurs, bien qu'affichées dans l'Observateur d'événements à chaque redémarrage, n'avaient aucun impact sur le fonctionnement de Windows et pouvaient être ignorées en attendant le correctif.

**Points Clés :**

*   Un dysfonctionnement dans le composant CertificateServicesClient (CertEnroll) de Windows causait des messages d'erreur trompeurs.
*   Ces erreurs étaient liées à la non-prise en charge d'une fonctionnalité en cours de développement, le 'Microsoft Pluton Cryptographic Provider'.
*   Microsoft avait initialement conseillé aux utilisateurs d'ignorer ces alertes, confirmant qu'elles n'affectaient pas les processus actifs de Windows.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. Le problème décrit est une erreur de logique logicielle plutôt qu'une faille de sécurité exploitable.

**Recommandations :**

*   Les utilisateurs affectés par ces erreurs peuvent désormais attendre le déploiement du correctif.
*   La mise à jour KB5064081, publiée le 29 août 2025, inclut cette résolution pour les appareils grand public et professionnels.
*   Le correctif sera déployé progressivement sur les appareils gérés par Microsoft et devrait être généralisé dans les quatre semaines suivant sa publication. Les futures mises à jour de sécurité et non-sécurité intégreront cette correction par défaut.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-bug-behind-windows-certificate-enrollment-errors/){:target="_blank"}
