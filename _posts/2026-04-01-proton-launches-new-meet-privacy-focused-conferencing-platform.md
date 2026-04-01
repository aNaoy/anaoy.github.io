---
title: 'Proton launches new "Meet" privacy-focused conferencing platform'
date: 2026-04-01
permalink: /posts/2026/04/01/proton-launches-new-meet-privacy-focused-conferencing-platform/
tags:
- veille-cyber
- bleepingcomp
---
### Proton Meet : Une alternative sécurisée pour la visioconférence

Proton lance « Meet », une plateforme de visioconférence axée sur la confidentialité, conçue pour contrer les risques liés à la surveillance, à la vente de données publicitaires et à l'entraînement des modèles d'IA à partir des conversations des utilisateurs.

**Points clés :**
*   **Chiffrement de bout en bout (E2EE) :** Utilisation du protocole open source *Messaging Layer Security* (MLS).
*   **Architecture sécurisée :** Les données sont chiffrées côté client ; Proton n'a aucun accès aux contenus (flux audio/vidéo ou texte).
*   **Confidentialité totale :** Aucune conservation des métadonnées (qui appelle qui, adresses IP). Le service est conforme au RGPD et au CCPA.
*   **Accessibilité :** Gratuit (jusqu'à 50 participants, réunions d'une heure) sans nécessité de compte Proton. Intégration possible avec Google et Microsoft Calendar.
*   **Mécanismes de protection :** Authentification via le protocole *Secure Remote Password* (SRP) et gestion des clés par rotation à chaque changement de participant (garantissant le secret persistants).

**Vulnérabilités :**
*   Aucune vulnérabilité logicielle (CVE) n'est identifiée à ce jour. Le risque principal réside dans la compromission du lien de réunion par un tiers.

**Recommandations :**
*   **Verrouillage des sessions :** Verrouiller la réunion une fois que tous les participants attendus sont présents.
*   **Gestion des accès :** Exclure immédiatement tout participant non autorisé.
*   **Renouvellement :** Générer de nouveaux liens de réunion pour éviter toute réutilisation non souhaitée.

---
[Source](https://www.bleepingcomputer.com/news/security/proton-launches-new-meet-privacy-focused-conferencing-platform/){:target="_blank"}
