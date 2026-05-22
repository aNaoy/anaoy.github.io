---
title: 'CISA Security Leak'
date: 2026-05-22
permalink: /posts/2026/05/22/cisa-security-leak/
tags:
- veille-cyber
- schneier
---
### Fuite massive de données critiques à la CISA

Un sous-traitant de la Cybersecurity & Infrastructure Security Agency (CISA) a exposé par inadvertance des identifiants sensibles sur un dépôt GitHub public. Cette faille, considérée comme l'une des plus graves de l'histoire gouvernementale récente, a rendu accessibles des accès privilégiés aux comptes AWS GovCloud ainsi que des informations sur les processus internes de développement, de test et de déploiement logiciel de l'agence.

**Points clés :**
*   **Source de la fuite :** Un dépôt GitHub public maintenu par un prestataire externe de la CISA.
*   **Données compromises :** Identifiants pour des comptes AWS GovCloud à haut niveau de privilèges et documentation détaillée sur l'infrastructure interne.
*   **Gravité :** Risque critique d'infiltration des systèmes gouvernementaux via les accès exposés.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, la faille relevant d'une mauvaise gestion des secrets et d'une exposition involontaire par erreur humaine (fuite de configuration).

**Recommandations :**
*   **Audit immédiat :** Révoquer et renouveler immédiatement toutes les clés, mots de passe et jetons d'accès exposés.
*   **Gestion des secrets :** Automatiser la détection de secrets (hardcoded credentials) dans les dépôts de code via des outils de scan (Secret Scanning).
*   **Contrôle des tiers :** Renforcer les politiques de sécurité imposées aux sous-traitants et auditer leurs pratiques de gestion de code source.
*   **Principe du moindre privilège :** Restreindre les accès AWS GovCloud pour limiter l'impact d'une éventuelle compromission future.

---
[Source](https://www.schneier.com/blog/archives/2026/05/cisa-security-leak.html){:target="_blank"}
