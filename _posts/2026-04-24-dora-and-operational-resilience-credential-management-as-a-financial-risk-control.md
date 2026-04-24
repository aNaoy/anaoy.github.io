---
title: 'DORA and operational resilience: Credential management as a financial risk control'
date: 2026-04-24
permalink: /posts/2026/04/24/dora-and-operational-resilience-credential-management-as-a-financial-risk-control/
tags:
- veille-cyber
- bleepingcomp
---
### DORA et gestion des identités : la sécurité des accès comme levier de résilience financière

Le règlement DORA (*Digital Operational Resilience Act*), entré en application le 17 janvier 2025, transforme la gestion des accès et des identifiants en une obligation de conformité légale sous l'Article 9. Dans le secteur financier, le vol d'identifiants reste le vecteur d'attaque principal, entraînant une persistance moyenne des menaces de 186 jours avant détection.

#### Points clés
*   **Responsabilité accrue :** La compromission d'identifiants n'est plus seulement un incident de sécurité, mais une faille de résilience opérationnelle impactant la continuité de service.
*   **Périmètre étendu :** Les institutions financières sont responsables de la sécurité des accès de leurs tiers (fournisseurs ICT). Une faille chez un partenaire (ex: cas Snowflake) engage la responsabilité réglementaire de l'entité financière.
*   **Obligations de reporting :** En cas d'incident, DORA impose des délais de notification stricts (4h, 72h, 1 mois) sous l'Article 19.

#### Vulnérabilités critiques
*   **Usage d'identifiants compromis :** Principal vecteur d'entrée, souvent facilité par des *infostealers* (Lumma, StealC, RedLine) et l'achat d'accès sur le marché noir.
*   **Absence de MFA phishing-resistant :** L'utilisation de SMS ou de codes TOTP standards, vulnérables aux attaques de type *Adversary-in-the-Middle* (AiTM).
*   **Gestion défaillante des privilèges :** Maintien de privilèges permanents et présence de comptes dormants, facilitant le mouvement latéral des attaquants.

#### Recommandations stratégiques (Conformité Article 9)
1.  **Généraliser le MFA résistant au phishing :** Implémenter des standards type FIDO2/WebAuthn (clés de sécurité, passkeys) pour tous les accès, en priorité pour les comptes à hauts privilèges.
2.  **Appliquer le principe du moindre privilège :** Mettre en œuvre le provisionnement *Just-in-Time* (JIT) pour limiter les accès aux besoins stricts et temporaires.
3.  **Centraliser et chiffrer les accès :** Utiliser des solutions de gestion des mots de passe (vaulting) permettant une traçabilité complète des accès (logs immuables).
4.  **Audit et monitoring continu :** Automatiser la détection de comportements anormaux (géolocalisation, heures atypiques) et documenter rigoureusement les contrôles pour répondre aux exigences des auditeurs.
5.  **Gouvernance des tiers :** Exiger contractuellement et auditer l'alignement des fournisseurs ICT sur ces standards d'authentification robuste.

---
[Source](https://www.bleepingcomputer.com/news/security/dora-and-operational-resilience-credential-management-as-a-financial-risk-control/){:target="_blank"}
