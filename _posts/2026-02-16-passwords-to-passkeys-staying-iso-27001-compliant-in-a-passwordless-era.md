---
title: 'Passwords to passkeys: Staying ISO 27001 compliant in a passwordless era'
date: 2026-02-16
permalink: /posts/2026/02/16/passwords-to-passkeys-staying-iso-27001-compliant-in-a-passwordless-era/
tags:
- veille-cyber
- bleepingcomp
---
**Passkeys : La nouvelle ère de l'authentification sécurisée et la conformité ISO 27001**

L'adoption des passkeys marque une évolution significative par rapport aux mots de passe traditionnels, offrant une sécurité renforcée et une expérience utilisateur améliorée. Ce nouveau standard d'authentification, basé sur les technologies FIDO2 et WebAuthn, repose sur des paires de clés cryptographiques (publique et privée) stockées sur l'appareil de l'utilisateur, éliminant ainsi les risques liés au phishing et à la réutilisation des mots de passe.

**Points Clés :**

*   **Évolution nécessaire :** Les mots de passe sont devenus une vulnérabilité majeure, 49 % des incidents de sécurité étant liés à leur compromission (Verizon 2023 DBIR), et 84 % des utilisateurs réutilisant les mêmes identifiants.
*   **Fonctionnement des Passkeys :** Utilisation de clés cryptographiques (privée stockée localement, publique enregistrée auprès du service), garantissant que la clé privée ne quitte jamais l'appareil de l'utilisateur lors de l'authentification.
*   **Niveaux d'Assurance (AAL) :** Les passkeys répondent généralement aux exigences AAL2 ou AAL3 du NIST, offrant un niveau de sécurité supérieur aux authentifications par mot de passe.
*   **Types de Passkeys :** Passkeys liées à l'appareil (stockées dans du matériel sécurisé) et passkeys synchronisables (sauvegardées via des services cloud chiffrés).
*   **Adoption Croissante :** Plus de 15 milliards de comptes en ligne supportent désormais les passkeys, avec des entreprises comme Amazon et Google rapportant des millions d'utilisateurs.
*   **Bénéfices Opérationnels :** Réduction significative des coûts liés à la gestion des mots de passe (réinitialisations, appels au support) et amélioration de l'efficacité de l'authentification.
*   **Conformité Multi-Normes :** Les passkeys facilitent la conformité avec diverses réglementations telles que NIST AAL2/AAL3, PCI DSS 4.0, GDPR et SOC 2.

**Vulnérabilités et Défis :**

*   **Attaques par Rétrogradation (Downgrade Attacks) :** Les attaquants peuvent manipuler les interfaces pour forcer le retour à l'authentification par mot de passe.
*   **Attaques de Phishing sur Codes d'Appareil et sur Consentement OAuth :** Ces attaques peuvent contourner certaines protections des passkeys en exploitant l'implémentation ou le comportement de l'utilisateur.
*   **Complexité de la Récupération de Compte :** La perte d'un appareil sans sauvegarde de passkey peut rendre l'accès au compte très difficile, nécessitant des méthodes de récupération alternatives (e-mail, vérification manuelle, codes de récupération) qui ont leurs propres implications de sécurité.
*   **Environnements Hybrides :** La cohabitation de passkeys et de mots de passe pendant la transition crée une posture de sécurité incohérente, des défis de politique et des complexités pour les pistes d'audit.

**Recommandations pour la Conformité ISO 27001 :**

*   **Alignement avec les Contrôles Annexes A :**
    *   **A 5.15 (Contrôle d'accès) :** Définir la portée des passkeys selon le niveau de risque, documenter les procédures de secours et les politiques d'authentification temporaire.
    *   **A 5.17 (Informations d'authentification) :** Documenter le processus d'inscription, les exigences de chiffrement pour les clés publiques, les déclencheurs de ré-inscription et les contrôles d'accès à la gestion des données d'authentification.
    *   **A 8.5 (Authentification sécurisée) :** Démontrer la conformité MFA en expliquant comment les passkeys fournissent deux facteurs (possession + biométrie/PIN), expliquer la liaison cryptographique aux domaines et détailler l'implémentation technique des protocoles WebAuthn/FIDO2.
*   **Évaluation et Traitement des Risques :**
    *   Identifier les risques éliminés (phishing de mots de passe, réutilisation, attaques par force brute) et les nouveaux risques (perte d'appareil, verrouillage fournisseur, complexité de récupération, attaques par rétrogradation).
    *   Établir des procédures de surveillance pour les nouveaux vecteurs d'attaque.
*   **Mise en Œuvre d'Entreprise :** Les plateformes de gestion devraient supporter l'authentification WebAuthn, des politiques flexibles, la vérification par e-mail, et des pistes d'audit détaillées.
*   **Bonnes Pratiques :** Prioriser par risque (comptes privilégiés d'abord), maintenir une défense en profondeur, planifier la transition avec des échéances claires, anticiper la récupération de compte, et documenter méticuleusement toutes les procédures et architectures.

---
[Source](https://www.bleepingcomputer.com/news/security/passwords-to-passkeys-staying-iso-27001-compliant-in-a-passwordless-era/){:target="_blank"}
