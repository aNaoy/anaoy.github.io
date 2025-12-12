---
title: 'New React RSC Vulnerabilities Enable DoS and Source Code Exposure'
date: 2025-12-12
permalink: /posts/2025/12/12/new-react-rsc-vulnerabilities-enable-dos-and-source-code-exposure/
tags:
- veille-cyber
- hackernews
---
### Nouvelles failles dans React Server Components

Deux nouvelles vulnérabilités ont été découvertes dans React Server Components (RSC). Elles peuvent permettre des attaques par déni de service (DoS) ou l'exposition du code source. Ces failles ont été identifiées par la communauté de sécurité lors de l'analyse des correctifs pour une vulnérabilité critique antérieure (CVE-2025-55182).

**Points clés :**

*   Les problèmes découverts font suite à la correction d'une vulnérabilité majeure précédemment exploitée.
*   Ces nouvelles failles sont le résultat de l'examen approfondi du code par les chercheurs suite à la divulgation initiale.

**Vulnérabilités :**

*   **CVE-2025-55184 (CVSS 7.5)** : Déni de service avant authentification causé par une désérialisation non sécurisée de requêtes HTTP vers les points d'accès Server Function. Cela peut entraîner une boucle infinie bloquant le serveur.
*   **CVE-2025-67779 (CVSS 7.5)** : Correction incomplète de CVE-2025-55184, ayant le même impact.
*   **CVE-2025-55183 (CVSS 5.3)** : Fuite d'informations permettant à une requête HTTP spécialement conçue d'exposer le code source de n'importe quelle Server Function. Cette attaque nécessite qu'une fonction expose un argument converti en chaîne de caractères.

**Versions affectées :**

*   **CVE-2025-55184 et CVE-2025-55183** : 19.0.0, 19.0.1, 19.1.0, 19.1.1, 19.1.2, 19.2.0 et 19.2.1.
*   **CVE-2025-67779** : 19.0.2, 19.1.3 et 19.2.2.

**Recommandations :**

*   Mettre à jour vers les versions **19.0.3, 19.1.4 et 19.2.3** dès que possible.

---
[Source](https://thehackernews.com/2025/12/new-react-rsc-vulnerabilities-enable.html){:target="_blank"}
