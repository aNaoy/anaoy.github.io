---
title: 'Two Chrome Extensions Caught Secretly Stealing Credentials from Over 170 Sites'
date: 2025-12-23
permalink: /posts/2025/12/23/two-chrome-extensions-caught-secretly-stealing-credentials-from-over-170-sites/
tags:
- veille-cyber
- hackernews
---
**Extensions Chrome Dangereuses : Capture d'Identifiants et Interception de Trafic**

Deux extensions Google Chrome, nommées "Phantom Shuttle" et publiées par le même développeur, ont été identifiées comme malveillantes. Ces extensions, présentées comme des outils de test de vitesse réseau pour les développeurs et le personnel du commerce extérieur, sont en réalité conçues pour intercepter le trafic réseau et voler les identifiants des utilisateurs.

**Points Clés :**

*   **Identifiants Volés :** Les extensions captent les identifiants de connexion (nom d'utilisateur, mot de passe) et d'autres données sensibles (numéros de carte bancaire, cookies d'authentification, historique de navigation, clés API, jetons d'accès) sur plus de 170 sites web ciblés.
*   **Interception de Trafic :** Elles fonctionnent comme des proxys Man-in-the-Middle, acheminant le trafic des utilisateurs via une infrastructure contrôlée par les attaquants.
*   **Modèle d'Abonnement Trompeur :** Les utilisateurs paient un abonnement, croyant acheter un service VPN légitime, ce qui renforce l'illusion de fonctionnement tout en masquant la véritable intention malveillante.
*   **Injection d'Authentification :** Les extensions injectent des identifiants proxy pré-codés lors des demandes d'authentification HTTP, contournant l'interaction utilisateur.
*   **Communication C2 :** Elles maintiennent une connexion régulière avec un serveur de commande et de contrôle pour exfiltrer les données volées.
*   **Ciblage Étendu :** Les domaines ciblés incluent des plateformes de développement, des services cloud, des solutions d'entreprise, des réseaux sociaux et des sites à contenu adulte.
*   **Opération de Longue Date :** L'opération semble être en cours depuis huit ans, avec des indices pointant vers une origine basée en Chine.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec identifiant CVE n'est mentionnée dans l'article. Les extensions exploitent des fonctionnalités légitimes de Chrome pour mener leurs actions malveillantes.

**Recommandations :**

*   **Utilisateurs :** Supprimer immédiatement les extensions "Phantom Shuttle" si elles sont installées.
*   **Équipes de Sécurité :**
    *   Mettre en place une liste blanche d'extensions autorisées.
    *   Surveiller les extensions proposant des systèmes de paiement par abonnement associés à des autorisations de proxy.
    *   Implémenter une surveillance réseau pour détecter les tentatives d'authentification proxy suspectes.

---
[Source](https://thehackernews.com/2025/12/two-chrome-extensions-caught-secretly.html){:target="_blank"}
