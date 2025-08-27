---
title: 'Referral Beware, Your Rewards are Mine'
date: 2025-08-27
permalink: /posts/2025/08/27/referral-beware-your-rewards-are-mine/
tags:
- veille-cyber
- zerodaysfans
---
## Sécuriser les Programmes de Parrainage : Vulnérabilités et Défenses

Les programmes de récompenses par parrainage, présents dans de nombreuses applications, manquent souvent de contrôles de sécurité adéquats. Ils peuvent être exploités par des attaquants pour obtenir des récompenses illégitimes, entraînant un impact financier direct ou indirect pour les entreprises. L'article détaille les implémentations courantes, les failles de sécurité associées et propose des recommandations pour un développement plus sûr.

### Implémentations Courantes

Les programmes de parrainage suivent généralement un processus où un utilisateur partage un code ou un lien, le nouveau participant s'inscrit, et les deux reçoivent des récompenses. Les méthodes d'attribution des parrainages incluent :

1.  **Paramètre d'URL vers Cookie** : Le code de parrainage dans l'URL est stocké dans un cookie lors de la visite, puis utilisé lors de l'inscription.
2.  **Paramètre d'URL vers Requête Initiée par le Client** : Le code est extrait de l'URL et envoyé via des requêtes JavaScript initiées par le client pour validation et application.
3.  **Code de Parrainage comme Code Promo** : Le code de parrainage est traité comme un code promotionnel, souvent appliqué lors du paiement.

### Points Clés et Vulnérabilités

L'analyse de plus de vingt programmes a révélé diverses failles de sécurité, notamment :

*   **Gadgets Client-Side** :
    *   **Injection de Cookie** : Permet de manipuler les valeurs de cookie, potentiellement via CRLF ou en définissant des attributs de chemin et de domaine spécifiques, menant à des attaques comme le "cookie tossing" ciblant les récompenses de parrainage.
    *   **Traversée de Chemin Client-Side (CSPT)** : L'exploitation de la manière dont les requêtes sont générées côté client peut mener à :
        *   **XSS (Cross-Site Scripting)** : Si la réponse d'une requête manipulée est injectée dans le DOM.
        *   **CSRF (Cross-Site Request Forgery)** : Si la CSPT peut être utilisée pour exécuter des requêtes modifiant l'état avec des méthodes appropriées.
*   **Défaillances de Logique Métier** : Des hypothèses erronées sur le comportement des utilisateurs ou les interactions entre différentes parties de l'application peuvent être exploitées pour contourner le flux prévu.
*   **Conditions de Course (Race Conditions)** : L'envoi simultané de multiples requêtes identiques pour l'application d'un code peut entraîner l'octroi de plusieurs récompenses pour une seule action.
*   **Détournement de Parrainage (Referral Hijacking)** : Une nouvelle attaque consistant à substituer le lien/code de parrainage original par celui de l'attaquant. La **fixation de cookie** est une méthode clé, où un attaquant peut associer un cookie de parrainage malveillant à un chemin spécifique, garantissant sa priorité lors des requêtes.

### Recommandations de Sécurité

Pour prévenir ces vulnérabilités, il est conseillé de :

1.  **Éviter les Hypothèses** : Ne pas présumer du comportement utilisateur ou du fonctionnement interne de l'application pour contrer les défaillances de logique métier.
2.  **Valider et Assainir les Entrées** : Nettoyer toutes les données fournies par l'utilisateur avant de les utiliser dans des cookies ou de les concaténer dans des requêtes client-side.
3.  **Gérer les Conditions de Course** : Mettre en œuvre des stratégies appropriées pour gérer la concurrence lors des opérations sensibles.
4.  **Prévenir le Détournement via Fixation de Cookie** : En plus de l'assainissement des cookies, empêcher d'autres méthodes de définition de cookies comme le XSS.

---
[Source](https://rhinosecuritylabs.com/research/referral-beware-your-rewards-are-mine-part-1/){:target="_blank"}
