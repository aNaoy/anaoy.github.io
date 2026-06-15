---
title: 'The Onboarding Password Mistake That Creates Unnecessary Risk'
date: 2026-06-15
permalink: /posts/2026/06/15/the-onboarding-password-mistake-that-creates-unnecessary-risk/
tags:
- veille-cyber
- hackernews
---
### Sécuriser l'intégration des employés : les risques liés aux mots de passe temporaires

L'intégration de nouveaux employés représente un vecteur d'attaque critique. Les méthodes traditionnelles de transmission des identifiants (e-mail, SMS, communication verbale) exposent les organisations à des risques d'interception et de fuites. De plus, la pratique consistant à utiliser des mots de passe temporaires est dangereuse : s'ils ne sont pas modifiés immédiatement, ils deviennent des points d'entrée persistants pour les attaquants.

**Points clés :**
*   **Vulnérabilité opérationnelle :** Les mots de passe temporaires sont souvent simplifiés pour faciliter la configuration, ce qui les rend prévisibles.
*   **Risque de persistance :** Un mot de passe temporaire oublié ou non réinitialisé par l'utilisateur devient un identifiant par défaut "permanent" et non sécurisé.
*   **Exemples d'incidents réels :**
    *   **Cyber Av3ngers (2023) :** Utilisation du mot de passe par défaut "1111" sur des contrôleurs logiques programmables (PLC) pour prendre le contrôle d'infrastructures hydrauliques.
    *   **Plateforme McHire (2025) :** Accès à des données sensibles de 64 millions de candidats via un compte administrateur protégé par le mot de passe "123456".

**Vulnérabilités associées :**
*   Usage de mots de passe par défaut (ex: `1111`, `123456`).
*   Absence de politique de réinitialisation forcée ou échec du processus de changement lors du premier accès.
*   Gestion des identifiants en texte clair sur des canaux non sécurisés.

**Recommandations :**
*   **Automatisation de l'enrôlement :** Éliminer la distribution de mots de passe temporaires. Utiliser des solutions permettant aux nouveaux utilisateurs de définir eux-mêmes leur mot de passe dès le premier accès via un processus sécurisé (ex: lien d'enrôlement vérifié par e-mail personnel ou téléphone).
*   **Sécurisation du cycle de vie :** Appliquer des politiques de mots de passe robustes dès le jour de l'intégration et assurer une protection contre l'utilisation de mots de passe compromis.
*   **Hygiène réseau :** Déconnecter les systèmes industriels ou de test exposés sur Internet et auditer systématiquement tout compte conservant des identifiants par défaut après la mise en production.

---
[Source](https://thehackernews.com/2026/06/the-onboarding-password-mistake-that.html){:target="_blank"}
