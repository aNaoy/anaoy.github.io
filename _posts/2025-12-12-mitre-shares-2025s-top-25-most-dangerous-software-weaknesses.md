---
title: 'MITRE shares 2025s top 25 most dangerous software weaknesses'
date: 2025-12-12
permalink: /posts/2025/12/12/mitre-shares-2025s-top-25-most-dangerous-software-weaknesses/
tags:
- veille-cyber
- bleepingcomp
---
### Les 25 Faiblesses Logicielles les Plus Dangereuses en 2025

**Points Clés :**

*   MITRE a publié sa liste annuelle des 25 faiblesses logicielles les plus critiques, basées sur l'analyse de plus de 39 000 vulnérabilités signalées entre juin 2024 et juin 2025.
*   Ces faiblesses sont des défauts, bogues ou erreurs dans le code, l'implémentation, l'architecture ou la conception d'un logiciel, exploitables par des attaquants pour prendre le contrôle de systèmes, voler des données ou provoquer des dénis de service.
*   La liste vise à aider les organisations à améliorer leurs stratégies de sécurité logicielle et les développeurs à adopter des pratiques de conception sécurisée ("Secure by Design").

**Vulnérabilités Principales (avec CVE si disponibles) :**

Les faiblesses les plus dangereuses pour 2025, selon leur gravité et leur fréquence, incluent :

1.  **CWE-79 : Cross-site Scripting (XSS)** (1er) - Absence de neutralisation des entrées lors de la génération de pages web.
2.  **CWE-89 : SQL Injection** (2ème) - Absence de neutralisation des éléments spéciaux utilisés dans une commande SQL.
3.  **CWE-352 : Cross-Site Request Forgery (CSRF)** (3ème) - Falsification de requêtes inter-sites.
4.  **CWE-862 : Missing Authorization** (4ème) - Absence d'autorisation.
5.  **CWE-787 : Out-of-bounds Write** (5ème) - Écriture hors des limites allouées.
6.  **CWE-22 : Path Traversal** (6ème) - Limitation inappropriée d'un nom de chemin vers un répertoire restreint.
7.  **CWE-416 : Use After Free** (7ème) - Utilisation après libération de mémoire.
8.  **CWE-125 : Out-of-bounds Read** (8ème) - Lecture hors des limites allouées.
9.  **CWE-78 : OS Command Injection** (9ème) - Absence de neutralisation des éléments spéciaux utilisés dans une commande OS.
10. **CWE-94 : Code Injection** (10ème) - Contrôle inapproprié de la génération de code.

D'autres nouvelles entrées notables incluent :
*   **CWE-120 : Classic Buffer Overflow** - Copie de tampon sans vérification de la taille de l'entrée.
*   **CWE-121 : Stack-based Buffer Overflow** - Dépassement de tampon basé sur la pile.
*   **CWE-122 : Heap-based Buffer Overflow** - Dépassement de tampon basé sur le tas.
*   **CWE-284 : Improper Access Control** - Contrôle d'accès inapproprié.
*   **CWE-639 : Authorization Bypass Through User-Controlled Key** - Contournement d'autorisation via une clé contrôlée par l'utilisateur.
*   **CWE-770 : Allocation of Resources Without Limits or Throttling** - Allocation de ressources sans limites ou limitation.

**Recommandations :**

*   Les organisations sont encouragées à examiner cette liste pour guider leurs stratégies de sécurité logicielle.
*   Les développeurs et les équipes de produits doivent identifier et corriger ces faiblesses critiques dans leurs logiciels.
*   Les équipes de sécurité doivent intégrer cette liste dans leurs processus de tests de sécurité applicative et de gestion des vulnérabilités.
*   Adopter des pratiques de conception sécurisée ("Secure by Design") est essentiel pour prévenir l'exploitation de ces faiblesses connues.

---
[Source](https://www.bleepingcomputer.com/news/security/mitre-shares-2025s-top-25-most-dangerous-software-weaknesses/){:target="_blank"}
