---
title: 'When attackers already have the keys, MFA is just another door to open'
date: 2026-04-09
permalink: /posts/2026/04/09/when-attackers-already-have-the-keys-mfa-is-just-another-door-to-open/
tags:
- veille-cyber
- bleepingcomp
---
### L'inefficacité structurelle du MFA face aux fuites de données

Les fuites massives de données, telles que celle ayant exposé près d'un million d'adresses e-mail chez Figure, ne constituent pas des incidents isolés, mais des points de départ pour des campagnes d'attaques automatisées. Les méthodes actuelles d'authentification multifacteur (MFA) échouent à contrer ces menaces car elles reposent sur une architecture vulnérable aux attaques de type « Adversary-in-the-Middle » (AiTM).

**Points clés :**
*   **Cycles d'attaque :** Une fois les identifiants récupérés, les attaquants utilisent le *credential stuffing* (test massif de mots de passe réutilisés), le phishing personnalisé par IA et l'ingénierie sociale auprès des help desks pour contourner les protections.
*   **Obsolescence du MFA traditionnel :** Les méthodes comme les codes SMS, les TOTP ou les notifications push sont inefficaces face aux proxys inversés (outils type Evilginx). Ces derniers interceptent les jetons de session en temps réel, rendant l'attaque invisible pour l'utilisateur.
*   **La faille humaine :** Le MFA traditionnel place l'utilisateur final comme rempart ultime contre l'attaque, or celui-ci est incapable de détecter une requête légitime détournée par un proxy.
*   **Limites du FIDO2/WebAuthn :** Bien que supérieurs, les passkeys synchronisés dans le cloud héritent des vulnérabilités de ces comptes, et les clés liées aux appareils prouvent la possession du matériel mais pas la présence physique de l'utilisateur autorisé.

**Recommandations pour une authentification résistante au phishing :**
Pour contrer efficacement ces vecteurs, l'architecture doit intégrer trois propriétés indissociables :
1.  **Liaison cryptographique à l'origine (Origin Binding) :** L'authentification doit être liée mathématiquement au domaine exact du service, bloquant toute tentative de spoofing.
2.  **Clés privées ancrées dans le matériel :** Les clés de signature ne doivent jamais pouvoir être exportées ou copiées.
3.  **Vérification biométrique réelle et locale :** Une authentification biométrique en temps réel est nécessaire pour garantir que l'individu autorisé est physiquement présent au moment précis de la connexion, sans possibilité de délégation ou d'exception.

---
[Source](https://www.bleepingcomputer.com/news/security/when-attackers-already-have-the-keys-mfa-is-just-another-door-to-open/){:target="_blank"}
