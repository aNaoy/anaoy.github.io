---
title: 'Russia-Linked Hackers Use Microsoft 365 Device Code Phishing for Account Takeovers'
date: 2025-12-19
permalink: /posts/2025/12/19/russia-linked-hackers-use-microsoft-365-device-code-phishing-for-account-takeovers/
tags:
- veille-cyber
- hackernews
---
### Nouvelle Technique de Phishing pour le Déroobage de Comptes Microsoft 365

Un groupe de pirates informatiques lié à la Russie utilise une méthode de phishing sophistiquée exploitant le flux d'authentification par code d'appareil de Microsoft 365. Cette campagne, active depuis septembre 2025 et surnommée UNK_AcademicFlare par Proofpoint, cible des organisations dans les secteurs gouvernemental, de la recherche, de l'enseignement supérieur et des transports aux États-Unis et en Europe.

Les attaquants compromettent des adresses électroniques d'organisations gouvernementales et militaires pour établir un contact initial, simulant un intérêt pour l'expertise de la cible afin d'organiser une fausse réunion. Ils proposent ensuite le partage d'un document via un lien, qui redirige vers une fausse page de connexion Microsoft OneDrive hébergée sur Cloudflare. L'utilisateur est invité à copier un code et à cliquer sur "Suivant".

Cette action le redirige vers le portail légitime d'authentification par code d'appareil de Microsoft. Une fois le code saisi, un jeton d'accès est généré, permettant aux attaquants de prendre le contrôle du compte de la victime. Cette technique a déjà été documentée par Microsoft et Volexity, et d'autres groupes comme TA2723 l'ont adoptée, utilisant des prétextes liés aux salaires. La disponibilité de kits de phishing comme Graphish et d'outils pour équipes rouges comme SquarePhish facilite la mise en œuvre de ces attaques, abaissant le seuil technique requis.

**Points Clés :**

*   Utilisation du flux d'authentification par code d'appareil de Microsoft 365 pour le vol d'identifiants.
*   Les attaquants exploitent des courriels compromis d'organisations gouvernementales et militaires.
*   Les cibles incluent des entités gouvernementales, des groupes de réflexion, l'enseignement supérieur et le transport.
*   La technique vise à obtenir un accès non autorisé aux données et au contrôle des comptes.
*   La disponibilité d'outils de phishing simplifie la mise en œuvre de ces attaques.

**Vulnérabilités :**

*   Absence de restrictions sur le flux d'authentification par code d'appareil, permettant son abus. (Pas de CVE spécifique mentionné pour cette méthode).

**Recommandations :**

*   Mettre en place une politique d'Accès Conditionnel dans Microsoft Entra ID (anciennement Azure AD) pour bloquer le flux de code d'appareil pour tous les utilisateurs.
*   Si le blocage général n'est pas possible, utiliser une politique basée sur une liste d'autorisation pour n'autoriser l'authentification par code d'appareil que pour les utilisateurs, systèmes d'exploitation ou plages d'adresses IP approuvés.

---
[Source](https://thehackernews.com/2025/12/russia-linked-hackers-use-microsoft-365.html){:target="_blank"}
