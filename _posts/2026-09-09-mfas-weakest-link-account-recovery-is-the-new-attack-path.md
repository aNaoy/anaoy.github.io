---
title: 'MFAs Weakest Link: Account Recovery Is the New Attack Path'
date: 2026-09-09
permalink: /posts/2026/09/09/mfas-weakest-link-account-recovery-is-the-new-attack-path/
tags:
- veille-cyber
- bleepingcomp
---
### Le support informatique : le nouveau vecteur d'attaque privilégié

Alors que l'authentification multifacteur (MFA) renforce la sécurité des accès, les attaquants contournent désormais ces protections en ciblant les procédures de récupération de compte. Le service desk est devenu un maillon faible critique : en manipulant les agents par ingénierie sociale, les pirates peuvent réinitialiser des mots de passe ou transférer des accès MFA vers leurs propres appareils.

**Points clés :**
* **Déplacement de la menace :** La complexité croissante des mécanismes de MFA incite les cybercriminels à cibler les processus humains plutôt que techniques.
* **Vulnérabilité des processus de secours :** Le support informatique représente une porte d'entrée majeure si les méthodes de vérification d'identité sont trop laxistes (ex: questions de sécurité facilement devinables).
* **Impact opérationnel :** Les attaques par usurpation d'identité (type *Scattered Spider*) peuvent mener à des compromissions réseau à grande échelle et à des pertes financières significatives, comme illustré par l'incident chez Marks & Spencer.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique, car il s'agit d'une vulnérabilité liée aux **processus organisationnels (ingénierie sociale)** et au manque de rigueur dans l'authentification des requêtes adressées au service desk.

**Recommandations :**
* **Moderniser la vérification d'identité :** Remplacer les méthodes basées sur des questions personnelles par des processus de vérification à haute assurance (ex: MFA imposé avant toute réinitialisation).
* **Intégrer le support dans le périmètre de sécurité :** Considérer le service desk comme une fonction critique de gestion des identités.
* **Automatiser et auditer :** Utiliser des outils qui exigent une preuve d'identité forte avant d'autoriser une action sensible (reset, déverrouillage) et intégrer ces événements de vérification dans les plateformes SIEM pour assurer une traçabilité complète.

---
[Source](https://www.bleepingcomputer.com/news/security/mfas-weakest-link-account-recovery-is-the-new-attack-path/){:target="_blank"}
