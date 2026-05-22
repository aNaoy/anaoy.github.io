---
title: 'Lawmakers Demand Answers as CISA Tries to Contain Data Leak'
date: 2026-05-22
permalink: /posts/2026/05/22/lawmakers-demand-answers-as-cisa-tries-to-contain-data-leak/
tags:
- veille-cyber
- krebs
---
### Fuite massive de données sensibles à la CISA : le Congrès exige des comptes

La Cybersecurity & Infrastructure Security Agency (CISA) est sous le feu des critiques après qu'un sous-traitant a exposé par erreur de nombreuses informations confidentielles sur un dépôt GitHub public nommé « Private-CISA ». Ces secrets, incluant des clés AWS GovCloud et des accès administrateur, étaient stockés en texte brut depuis novembre 2025. Malgré le retrait du dépôt, la lenteur de l'agence à invalider les accès compromise et le manque de transparence soulèvent des inquiétudes majeures au Congrès américain quant à la culture de sécurité interne et à la gestion des prestataires de l'agence.

**Points clés :**
* **Exposition volontaire par négligence :** Le sous-traitant a délibérément désactivé les mécanismes de protection de GitHub contre l'exposition de secrets pour synchroniser ses fichiers de travail personnels.
* **Risque d'intrusion :** Des clés RSA exposées permettaient un accès total aux dépôts privés, aux pipelines CI/CD et aux paramètres d'administration de l'organisation GitHub de la CISA.
* **Contexte organisationnel :** Cet incident survient dans un climat de fragilité interne, marqué par une perte importante d'effectifs et de cadres dirigeants.
* **Surveillance active :** Les chercheurs en sécurité et les acteurs malveillants surveillent en temps réel les flux de données GitHub pour identifier les identifiants exposés.

**Vulnérabilités :**
* **Fuite de secrets (Secret Sprawl) :** Exposition de jetons API, mots de passe et clés SSH en clair dans des dépôts de code public.
* **Absence de contrôle des endpoints :** Utilisation de comptes personnels pour manipuler des données gouvernementales sensibles échappant à la surveillance de l'agence.
* **CVE :** Aucune CVE spécifique n'est associée, car il s'agit d'une erreur de configuration humaine et d'une mauvaise gestion des politiques de sécurité (défaut de « secret scanning » appliqué strictement au niveau organisationnel).

**Recommandations :**
* **Automatisation du blocage :** Imposer des politiques organisationnelles strictes sur les plateformes de code interdisant la désactivation des protections contre l'exposition de secrets.
* **Rotation immédiate des secrets :** En cas de fuite, ne pas se limiter aux clés identifiées, mais procéder à une rotation massive de tous les secrets liés aux infrastructures critiques.
* **Renforcement de la gouvernance des prestataires :** Établir des contrôles d'accès basés sur le principe du moindre privilège et restreindre l'utilisation de plateformes tierces non managées pour le stockage de code ou de données confidentielles.
* **Surveillance proactive :** Utiliser des outils de détection de fuites (comme TruffleHog ou GitGuardian) pour surveiller en continu les dépôts publics et détecter les exfiltrations accidentelles avant qu'elles ne soient exploitées par des adversaires.

---
[Source](https://krebsonsecurity.com/2026/05/lawmakers-demand-answers-as-cisa-tries-to-contain-data-leak/){:target="_blank"}
