---
title: 'MFA matters… But it isn’t enough on its own'
date: 2025-08-07
permalink: /posts/2025/08/07/mfa-matters-but-it-isnt-enough-on-its-own/
tags:
- veille-cyber
- bleepingcomp
---
**La Double Défense : MFA et Hygiène des Mots de Passe**

Bien que l'authentification multifacteur (MFA) soit essentielle pour renforcer la sécurité des accès et bloquer la majorité des attaques par compromission de comptes, elle ne suffit pas seule. Une approche de sécurité des identités doit impérativement combiner une gestion rigoureuse des mots de passe avec la MFA.

**Points Clés :**

*   **Efficacité de la MFA :** La MFA est reconnue pour bloquer plus de 99% des attaques automatisées de credential stuffing et de phishing en ajoutant une barrière supplémentaire à l'authentification. Elle est également alignée sur les normes réglementaires comme celles du NIST.
*   **Vulnérabilité des Mots de Passe :** La MFA ne résout pas les problèmes liés aux mots de passe faibles, réutilisés ou compromis. Si un attaquant parvient à contourner la MFA, un mot de passe médiocre devient la porte d'entrée vers les systèmes.
*   **Scénarios de Contournement :** Les attaquants utilisent diverses techniques pour contourner la MFA, telles que la fatigue de la MFA (bombardement de notifications), le SIM swapping, l'ingénierie sociale auprès du support informatique, le vol de sessions ou l'exploitation des méthodes de récupération alternatives.
*   **Approche en Couches :** Une stratégie de sécurité robuste nécessite de multiples couches de défense. La combinaison de mots de passe forts et de MFA sur tous les points d'accès critiques crée des obstacles significatifs pour les adversaires.

**Vulnérabilités et Attaques Courantes :**

*   **Fatigue de la MFA / Bombardement de notifications :** Les attaquants submergent l'utilisateur avec des demandes d'approbation MFA jusqu'à ce qu'une soit acceptée.
*   **SIM Swap / SMS Hijacking :** L'interception des codes envoyés par SMS, le second facteur d'authentification, permet de usurper l'identité de l'utilisateur.
*   **Ingénierie Sociale au Support Informatique :** Des attaquants se font passer pour des utilisateurs bloqués afin de désactiver la MFA ou de réinitialiser les identifiants (ex: attaque MGM Resorts).
*   **Vol de Sessions et de Tokens :** L'interception de cookies ou de tokens de session via des malwares ou des attaques "man-in-the-middle" permet de contourner l'authentification.
*   **Exploitation des Méthodes de Récupération :** Les questions de sécurité, les codes de récupération et les réinitialisations par e-mail sont souvent moins sécurisés et peuvent être exploités.

**Recommandations :**

*   **Activer la MFA :** L'implémentation de la MFA sur tous les points d'accès critiques (connexion Windows, VPN, RDP, portails cloud) est primordiale.
*   **Mots de Passe Robustes :** Imposer une longueur minimale (au moins 15 caractères, privilégier les phrases de passe) et des politiques de complexité.
*   **Blocage des Identifiants Compromis :** Intégrer des vérifications en temps réel pour empêcher l'utilisation de mots de passe déjà compromis dans des fuites de données.
*   **Sécurisation du Support Informatique :** Mettre en place une authentification MFA secondaire pour confirmer l'identité de toute personne contactant le service d'assistance.
*   **Surveillance des Connexions :** Monitorer les journaux pour détecter les schémas de connexion inhabituels et déclencher une authentification supplémentaire si nécessaire.

---
[Source](https://www.bleepingcomputer.com/news/security/mfa-matters-but-it-isnt-enough-on-its-own/){:target="_blank"}
