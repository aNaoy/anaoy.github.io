---
title: 'MFA matters… But it isn’t enough on its own'
date: 2025-08-06
permalink: /posts/2025/08/06/mfa-matters-but-it-isnt-enough-on-its-own/
tags:
- veille-cyber
- bleepingcomp
---
**Authentification à deux facteurs : Indispensable mais insuffisant**

L'authentification multifacteur (MFA) est essentielle pour renforcer la sécurité des accès et peut bloquer plus de 99 % des attaques automatisées de vol d'identifiants et de phishing. Elle ajoute une barrière supplémentaire, rendant les mots de passe volés insuffisants pour un accès non autorisé. Elle aide également à la conformité réglementaire et renforce la confiance des utilisateurs.

Cependant, l'MFA ne suffit pas à elle seule. Une mauvaise gestion des mots de passe (faibles, réutilisés ou compromis) laisse une faille critique. Les attaquants peuvent contourner l'MFA par divers moyens, rendant le mot de passe initial vulnérable. De plus, les procédures de récupération d'accès (réinitialisation de mot de passe, remplacement d'appareil) peuvent revenir à une authentification par mot de passe seul si celui-ci est faible.

**Tactiques utilisées par les attaquants pour contourner l'MFA :**

*   **Fatigue MFA (MFA prompt-bombing)** : bombarder l'utilisateur de notifications pour qu'il en approuve une par lassitude.
*   **SIM swap & SMS hijack** : intercepter les codes envoyés par SMS sur le téléphone compromis.
*   **Ingénierie sociale au niveau du support** : tromper le personnel du support pour qu'il désactive l'MFA ou réinitialise les identifiants (ex: cas MGM Resorts).
*   **Détournement de session & vol de tokens** : intercepter des cookies ou des tokens de session via des malwares ou des attaques "man-in-the-middle".
*   **Exploitation des méthodes de secours** : utiliser des questions de sécurité faibles, des codes de récupération ou des réinitialisations par email.

**Points clés et recommandations :**

*   **Les avantages de l'MFA sont indéniables** : barrière supplémentaire, résistance au phishing, conformité, confiance utilisateur, évitement des coûts liés aux violations.
*   **L'MFA peut être contournée** : ne pas se reposer uniquement sur l'MFA.
*   **Adopter une approche multicouche** : combiner des mots de passe robustes avec l'MFA pour tous les points d'accès critiques (connexion Windows, VPN, bureau à distance, portails cloud).
*   **Renforcer l'hygiène des mots de passe** :
    *   Activer l'MFA partout.
    *   Imposer une longueur minimale (au moins 15 caractères pour les phrases de passe).
    *   Bloquer les identifiants compromis en temps réel (basé sur des listes de fuites de données).
    *   Protéger le service desk en imposant une double authentification pour les demandes d'assistance.
    *   Surveiller les schémas de connexion inhabituels pour détecter les anomalies.

Ensemble, des politiques de mots de passe solides et l'MFA constituent une stratégie d'authentification résiliente pour une meilleure sécurité.

**Vulnérabilités mentionnées (sans CVE spécifiques dans l'article) :**

*   Mots de passe faibles, réutilisés ou compromis.
*   Contournement de l'MFA par fatigue, ingénierie sociale, détournement de session, etc.
*   Vulnérabilités des méthodes de récupération de compte.
*   Vulnérabilité des codes envoyés par SMS.

---
[Source](https://www.bleepingcomputer.com/news/security/mfa-matters-but-it-isnt-enough-on-its-own/){:target="_blank"}
