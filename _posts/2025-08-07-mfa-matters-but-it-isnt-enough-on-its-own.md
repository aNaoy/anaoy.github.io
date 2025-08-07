---
title: 'MFA matters… But it isn’t enough on its own'
date: 2025-08-07
permalink: /posts/2025/08/07/mfa-matters-but-it-isnt-enough-on-its-own/
tags:
- veille-cyber
- bleepingcomp
---
## L'authentification multifacteur : une protection nécessaire mais insuffisante

L'authentification multifacteur (MFA) est devenue une norme pour renforcer la sécurité des accès, bloquant plus de 99% des attaques automatisées de déduction d'identifiants et de phishing. Elle ajoute une barrière supplémentaire au traditionnel couple nom d'utilisateur/mot de passe, améliore la résilience face au phishing et aide à la conformité réglementaire.

Cependant, l'MFA seul ne suffit pas. Les identifiants faibles, réutilisés ou compromis constituent une faille critique. Si un attaquant parvient à contourner l'MFA, ces mêmes identifiants deviennent la clé d'accès aux systèmes. De plus, l'MFA peut être contournée par diverses tactiques.

### Points clés :

*   L'MFA réduit considérablement le risque d'accès non autorisé.
*   Une mauvaise hygiène des mots de passe affaiblit l'efficacité de l'MFA.
*   Une approche de sécurité multicouche, combinant une gestion rigoureuse des mots de passe et l'MFA, est essentielle.

### Vulnérabilités et tactiques d'attaque :

*   **Fatigue de l'MFA (MFA prompt-bombing)** : bombardement de notifications push pour pousser l'utilisateur à approuver.
*   **SIM swapping et détournement de SMS** : interception des codes envoyés par SMS.
*   **Ingénierie sociale au niveau du service d'assistance** : manipulation du personnel pour désactiver l'MFA ou réinitialiser des identifiants (mention de la faille chez MGM Resorts).
*   **Vol de session et d'identifiants de session (tokens)** : interception de cookies ou de tokens par malware ou attaques de type "man-in-the-middle".
*   **Exploitation des méthodes de secours** : questions de sécurité, codes de récupération ou réinitialisations par e-mail souvent moins sécurisées.

### Recommandations :

*   **Activer l'MFA** sur tous les points d'accès critiques (connexion Windows, VPN, bureau à distance, portails cloud).
*   **Appliquer des règles de mots de passe robustes** : longueur minimale (au moins 15 caractères, privilégier les phrases de passe) et complexité.
*   **Bloquer les identifiants compromis connus** : intégrer des vérifications en temps réel avec des listes de mots de passe divulgués.
*   **Sécuriser le service d'assistance** en exigeant une authentification multifacteur pour confirmer l'identité des personnes contactant le support.
*   **Surveiller les schémas de connexion inhabituels** en analysant conjointement les journaux de mots de passe et d'MFA pour détecter les anomalies et déclencher une authentification renforcée.

---
[Source](https://www.bleepingcomputer.com/news/security/mfa-matters-but-it-isnt-enough-on-its-own/){:target="_blank"}
