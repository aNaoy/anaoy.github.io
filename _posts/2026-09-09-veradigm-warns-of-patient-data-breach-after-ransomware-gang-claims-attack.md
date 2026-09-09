---
title: 'Veradigm warns of patient data breach after ransomware gang claims attack'
date: 2026-09-09
permalink: /posts/2026/09/09/veradigm-warns-of-patient-data-breach-after-ransomware-gang-claims-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données chez Veradigm : Le groupe "The Gentlemen" impliqué

La société de technologie de santé Veradigm a été victime d'une fuite de données suite à une compromission des identifiants d'un fournisseur tiers. Bien que Veradigm limite l'impact à une petite partie de sa clientèle, le groupe de rançongiciel "The Gentlemen" revendique le vol de 3,5 millions de dossiers de patients.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'identifiants légitimes volés à un fournisseur tiers pour accéder à une API de service client de Veradigm.
*   **Données exposées :** Informations personnelles et numéros de sécurité sociale (SSN). Les données cliniques et médicales sont restées sécurisées.
*   **Impact opérationnel :** Aucun système interne, serveur ou base de données de Veradigm n'a été compromis au-delà de l'interface API ciblée.
*   **Menace en cours :** Le groupe "The Gentlemen", adepte de la double extorsion, menace de publier les données volées faute de paiement d'une rançon.

**Vulnérabilités :**
*   Le vecteur principal repose sur une **compromission d'identifiants (Credential Compromise)** chez un tiers, plutôt que sur une faille logicielle spécifique (CVE non applicable).
*   Risque lié à l'utilisation du malware **SystemBC** pour les accès par botnet et à l'usage de **"GentleKiller"** pour neutraliser les solutions EDR (Endpoint Detection and Response).

**Recommandations :**
*   **Sécurisation des accès tiers :** Appliquer strictement le principe du moindre privilège pour les accès API fournis aux partenaires et fournisseurs.
*   **Authentification forte :** Renforcer l'authentification des comptes tiers accédant aux interfaces critiques (MFA obligatoire).
*   **Surveillance des logs API :** Mettre en place une détection d'anomalies sur les accès aux API pour identifier rapidement une utilisation inhabituelle des identifiants.
*   **Gestion des risques fournisseurs :** Auditer régulièrement les politiques de sécurité des partenaires ayant un accès aux environnements de production ou aux données sensibles.

---
[Source](https://www.bleepingcomputer.com/news/security/veradigm-discloses-patient-data-breach-after-gentlemen-gang-claims-attack/){:target="_blank"}
