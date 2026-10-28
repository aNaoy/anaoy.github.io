---
title: 'Google to Allow One-Tap Android App Installs From Approved Third-Party Stores Outside U.S.'
date: 2026-10-28
permalink: /posts/2026/10/28/google-to-allow-one-tap-android-app-installs-from-approved-third-party-stores-outside-us/
tags:
- veille-cyber
- hackernews
---
### Expansion du programme "Registered App Stores" pour Android

À partir du 1er décembre, Google autorise les magasins d'applications tiers approuvés (en dehors des États-Unis) à proposer l'installation d'applications en un clic et les mises à jour en arrière-plan sur les appareils équipés d'Android 17 QPR2 ou version ultérieure.

**Points clés :**
*   **Conditions d'éligibilité :** Les boutiques doivent être enregistrées, vérifier l'identité de leurs développeurs et soumettre l'intégralité de leur catalogue à Google pour une analyse continue contre les logiciels malveillants.
*   **Transparence :** Bien que l'installation soit simplifiée, le consentement explicite de l'utilisateur reste obligatoire. Les téléchargements volumineux et les installations en arrière-plan doivent faire l'objet d'une notification visible.
*   **Responsabilité :** Les magasins tiers conservent l'entière responsabilité du contenu de leur catalogue. Google ne modère pas les applications, mais applique des frais supplémentaires si le taux d'applications malveillantes dépasse certains seuils (1% des tentatives d'installation ou 2% du catalogue).
*   **Contrôle administrateur :** Les administrateurs informatiques conservent la possibilité de bloquer l'utilisation de ces magasins sur les appareils gérés.
*   **Coûts :** L'adhésion au programme nécessite le paiement de frais annuels de 10 000 $.

**Vulnérabilités et risques :**
*   Aucun CVE spécifique n'est mentionné dans l'article.
*   **Risque inhérent :** Malgré les mesures de filtrage de Google, la dépendance envers des magasins tiers augmente la surface d'attaque potentielle. La sécurité repose sur la capacité des boutiques à empêcher l'introduction de logiciels malveillants dans leur catalogue et sur la réactivité de Google à détecter ces menaces lors des scans.

**Recommandations :**
*   **Pour les entreprises :** Utiliser les outils de gestion de flotte (MDM/EMM) pour bloquer l'installation des magasins tiers si la politique de sécurité interne l'exige.
*   **Pour les utilisateurs :** Maintenir les appareils à jour (Android 17 QPR2+) pour bénéficier des dernières protections liées au système de vérification des développeurs.
*   **Pour les magasins :** Utiliser l'API *Android Developer ID* fournie par Google pour s'assurer que chaque application provient d'un développeur vérifié et bloquer systématiquement les applications non conformes.

---
[Source](https://thehackernews.com/2026/10/google-to-allow-one-tap-android-app.html){:target="_blank"}
