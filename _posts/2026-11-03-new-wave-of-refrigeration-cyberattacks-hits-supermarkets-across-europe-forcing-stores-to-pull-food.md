---
title: 'New Wave of Refrigeration Cyberattacks Hits Supermarkets Across Europe, Forcing Stores to Pull Food'
date: 2026-11-03
permalink: /posts/2026/11/03/new-wave-of-refrigeration-cyberattacks-hits-supermarkets-across-europe-forcing-stores-to-pull-food/
tags:
- veille-cyber
- hackernews
---
### Cyberattaques massives contre les systèmes de réfrigération en Europe

Une vague de cyberattaques a visé les systèmes de contrôle de réfrigération de nombreux supermarchés à travers l'Europe (Belgique, Suède, Estonie, Pays-Bas, etc.), forçant les enseignes à jeter des produits frais et congelés par mesure de sécurité. Les attaquants accèdent aux contrôleurs de réfrigération connectés à Internet pour modifier les températures ou activer le mode dégivrage, provoquant un réchauffement des unités.

**Points clés :**
*   **Cibles :** Systèmes de gestion de réfrigération (principalement Danfoss, mais aussi Copeland).
*   **Méthode :** Accès distant aux contrôleurs via Internet, exploitation de mots de passe par défaut et absence de mise à jour des firmwares.
*   **Impact :** Pertes de denrées alimentaires et arrêts de service temporaires dans plusieurs enseignes (Delhaize, Carrefour, Intermarché, ICA, Coop, etc.).
*   **Contexte :** Les attaques utilisent des modes opératoires similaires à ceux observés en France en octobre 2026.

**Vulnérabilités identifiées :**
*   Exposition directe des contrôleurs sur Internet (adresse IP publique).
*   Utilisation de mots de passe par défaut.
*   Logiciels obsolètes (firmwares non mis à jour).
*   Appareils en fin de vie ne bénéficiant plus de correctifs de sécurité (ex : modèles Danfoss AK-SM 800 et AK-SC 355).
*   *Note : Aucune CVE spécifique n'est mentionnée dans l'article, le problème résidant dans la configuration et l'obsolescence matérielle.*

**Recommandations de sécurité :**
*   **Isolation réseau :** Déconnecter impérativement les dispositifs d'Internet. Restreindre l'accès à un réseau privé protégé ou à un VPN.
*   **Sécurisation des accès :** Modifier immédiatement tous les mots de passe par défaut et configurer le niveau de sécurité sur "Strict".
*   **Maintenance :** Appliquer les dernières mises à jour de firmware disponibles.
*   **Inventaire :** Recenser tous les appareils connectés et évaluer la nécessité réelle de leur connectivité.
*   **Récupération :** En cas de compromission, effectuer une réinitialisation d'usine, reconfigurer les systèmes et sécuriser l'accès avant toute remise en service.
*   **Filtrage :** En urgence, filtrer les adresses IP des prestataires via un pare-feu (mesure temporaire).

---
[Source](https://thehackernews.com/2026/11/second-wave-of-cyberattacks-hits.html){:target="_blank"}
