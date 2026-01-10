---
title: 'BreachForums hacking forum database leaked, exposing 324,000 accounts'
date: 2026-01-10
permalink: /posts/2026/01/10/breachforums-hacking-forum-database-leaked-exposing-324000-accounts/
tags:
- veille-cyber
- bleepingcomp
---
## Fuite de Données sur un Forum de Cybercriminalité

La base de données utilisateur du forum de cybercriminalité BreachForums a été compromise, révélant les informations de 323 988 membres. Ce forum, une plateforme dédiée à l'échange, la vente et la fuite de données volées, ainsi qu'à la proposition de services illégaux en cybersécurité, a déjà fait l'objet d'actions judiciaires et de fuites par le passé.

La divulgation récente comprend trois fichiers : un texte détaillant l'histoire de James, une base de données SQL (mybb_users) et la clé privée PGP du forum, bien que cette dernière soit protégée par un mot de passe. La base de données SQL contient des noms d'utilisateur, des dates d'inscription, des adresses IP et d'autres informations internes. Bien que la majorité des adresses IP soient des adresses locales, environ 70 296 enregistrements comportent des adresses IP publiques potentiellement exploitables par les forces de l'ordre et les chercheurs en cybersécurité.

L'administrateur de BreachForums a reconnu que la table des utilisateurs et la clé PGP ont été temporairement exposées dans un dossier non sécurisé durant une phase de restauration du forum, et que l'accès à ces données n'a été effectué qu'une seule fois.

### Points Clés :

*   **Compromission de BreachForums :** La base de données utilisateur du forum a été divulguée.
*   **Volume des données :** 323 988 enregistrements de membres exposés.
*   **Nature des données :** Noms d'utilisateur, dates d'inscription, adresses IP publiques pour une partie des utilisateurs, et informations internes.
*   **Clé PGP :** La clé privée du forum a été leakée mais est protégée par un mot de passe, limitant son exploitation immédiate pour la signature de messages officiels.
*   **Explication de l'administrateur :** La fuite est due à une exposition temporaire dans un dossier non sécurisé pendant une opération de restauration.

### Vulnérabilités :

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article concernant la cause directe de cette fuite, hormis l'exposition accidentelle d'un dossier.

### Recommandations :

*   Pour les utilisateurs de forums similaires : Utiliser des adresses e-mail jetables pour réduire les risques.
*   Pour les administrateurs de plateformes en ligne : Mettre en place des procédures de sécurité rigoureuses pour éviter l'exposition accidentelle de données sensibles, notamment lors des opérations de maintenance ou de restauration.
*   Les forces de l'ordre et les chercheurs en cybersécurité peuvent potentiellement utiliser les adresses IP publiques divulguées pour des enquêtes.

---
[Source](https://www.bleepingcomputer.com/news/security/breachforums-hacking-forum-database-leaked-exposing-324-000-accounts/){:target="_blank"}
