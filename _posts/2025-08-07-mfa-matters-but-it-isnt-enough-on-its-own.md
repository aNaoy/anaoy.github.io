---
title: 'MFA matters… But it isn’t enough on its own'
date: 2025-08-07
permalink: /posts/2025/08/07/mfa-matters-but-it-isnt-enough-on-its-own/
tags:
- veille-cyber
- bleepingcomp
---
## Sécurité d'accès renforcée : Au-delà de l'authentification multi-facteurs

L'authentification multi-facteurs (MFA) est cruciale pour sécuriser les accès en ajoutant une couche de protection contre les attaques par prise de contrôle de compte. Elle bloque une part prépondérante des attaques automatisées de combinaison d'identifiants et de phishing. Cependant, l'MFA seule n'est pas infaillible et peut être contournée. Une dépendance excessive à l'MFA peut engendrer une négligence concernant la sécurité des mots de passe, qui restent le premier point d'entrée pour les attaquants.

### Points Clés :

*   L'MFA est un standard de facto pour renforcer la sécurité des accès.
*   Il protège contre la majorité des attaques par credential stuffing et phishing.
*   Même avec l'MFA, des mots de passe faibles, réutilisés ou compromis représentent une vulnérabilité critique.
*   Les attaquants peuvent contourner l'MFA par diverses méthodes, telles que l'ingénierie sociale, le SIM swapping ou l'exploitation des méthodes de récupération de compte.
*   Une approche de sécurité multicouche combinant une gestion rigoureuse des mots de passe et l'MFA est essentielle.

### Vulnérabilités exploitées par les attaquants :

*   **Fatigue de l'MFA (MFA prompt-bombing)** : Bombarder l'utilisateur de notifications push jusqu'à ce qu'il en approuve une par lassitude.
*   **SIM Swap & SMS Hijack** : Exploiter la vulnérabilité des codes à usage unique envoyés par SMS en prenant le contrôle du numéro de téléphone.
*   **Ingénierie Sociale au Support Technique** : Usurper l'identité d'un utilisateur légitime pour désactiver l'MFA ou réinitialiser les identifiants auprès du service d'assistance. L'article cite le piratage de MGM Resorts comme exemple.
*   **Vol de Session & Token** : Intercepter ou voler des cookies et des jetons de session via des malwares ou des attaques de type "man-in-the-middle" pour contourner les deux facteurs d'authentification.
*   **Exploitation des Méthodes de Sauvegarde** : Utiliser des questions de sécurité obsolètes, des codes de récupération ou des réinitialisations par email, souvent moins sécurisées, pour accéder aux comptes.

### Recommandations :

*   **Implémenter l'MFA partout** : Activer l'MFA pour toutes les connexions critiques (connexion Windows, VPN, bureau à distance, portails cloud).
*   **Renforcer la politique des mots de passe** : Imposer une longueur minimale de 15 caractères pour les mots de passe et encourager l'utilisation de phrases de passe.
*   **Bloquer les identifiants compromis** : Utiliser des listes de mots de passe divulgués en temps réel pour empêcher les utilisateurs de choisir des identifiants déjà compromis.
*   **Sécuriser le service desk** : Mettre en place une authentification secondaire (MFA) pour toute personne contactant le service d'assistance.
*   **Surveiller les modèles de connexion inhabituels** : Détecter les anomalies (connexions depuis des lieux ou appareils inconnus) et déclencher une authentification supplémentaire si nécessaire.

Il est primordial de ne jamais considérer l'MFA comme un substitut à une bonne hygiène des mots de passe. La combinaison d'une gestion stricte des mots de passe et de l'MFA constitue une stratégie d'authentification résiliente.

---
[Source](https://www.bleepingcomputer.com/news/security/mfa-matters-but-it-isnt-enough-on-its-own/){:target="_blank"}
