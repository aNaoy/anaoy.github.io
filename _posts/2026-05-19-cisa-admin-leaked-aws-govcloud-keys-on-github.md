---
title: 'CISA Admin Leaked AWS GovCloud Keys on Github'
date: 2026-05-19
permalink: /posts/2026/05/19/cisa-admin-leaked-aws-govcloud-keys-on-github/
tags:
- veille-cyber
- krebs
---
### Fuite massive de données sensibles : CISA expose ses accès AWS sur GitHub

Un entrepreneur travaillant pour la Cybersecurity & Infrastructure Security Agency (CISA) a exposé par erreur un dépôt GitHub public contenant des identifiants hautement privilégiés pour des comptes AWS GovCloud, ainsi que de nombreux mots de passe en clair pour des systèmes internes de l'agence.

**Points clés :**
*   **Origine de l'incident :** Un entrepreneur de la société Nightwing utilisait un dépôt GitHub nommé « Private-CISA » comme espace de travail pour synchroniser des fichiers entre différents environnements.
*   **Nature des données exposées :** Clés AWS GovCloud, jetons d'accès, mots de passe en texte clair, journaux internes et détails sur le cycle de développement logiciel (DevSecOps) de l'agence.
*   **Négligence opérationnelle :** L'administrateur avait volontairement désactivé les fonctionnalités de détection de secrets de GitHub et utilisait des mots de passe faibles (ex: nom du système + année).
*   **Réponse tardive :** Bien que le dépôt ait été supprimé suite à un signalement, les clés AWS sont restées valides pendant 48 heures supplémentaires après l'alerte.

**Vulnérabilités :**
*   **Exposition de secrets (Hardcoded Credentials) :** Stockage de clés API et de mots de passe dans un système de gestion de versions public.
*   **Désactivation des contrôles de sécurité :** Désactivation délibérée des outils de scan automatique des secrets fournis par GitHub.
*   **Absence de rotation des secrets :** Maintien de la validité des clés d'accès plusieurs jours après la notification de leur compromission.
*   *(Note : Aucune CVE n'est associée à cet incident, car il s'agit d'une erreur de configuration humaine et non d'une faille logicielle.)*

**Recommandations :**
*   **Implémentation du "Secret Scanning" :** Activer systématiquement les outils de détection de secrets sur les plateformes de développement et bloquer les commits contenant des identifiants.
*   **Gestion centralisée des identifiants :** Proscrire le stockage de secrets en clair dans des fichiers (CSV, texte) et privilégier l'utilisation de gestionnaires de secrets (AWS Secrets Manager, Vault).
*   **Renforcement de la politique de sécurité des accès :** Imposer l'authentification multifacteur (MFA) et procéder à une rotation régulière et automatique des clés d'accès aux infrastructures cloud.
*   **Surveillance et révocation :** Mettre en place des procédures de réponse aux incidents permettant la révocation immédiate et automatique de tout jeton ou clé suspecté d'être exposé.

---
[Source](https://krebsonsecurity.com/2026/05/cisa-admin-leaked-aws-govcloud-keys-on-github/){:target="_blank"}
