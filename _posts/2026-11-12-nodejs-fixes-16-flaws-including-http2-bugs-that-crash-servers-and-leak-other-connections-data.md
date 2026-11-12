---
title: 'Node.js Fixes 16 Flaws, Including HTTP/2 Bugs That Crash Servers and Leak Other Connections Data'
date: 2026-11-12
permalink: /posts/2026/11/12/nodejs-fixes-16-flaws-including-http2-bugs-that-crash-servers-and-leak-other-connections-data/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans Node.js : Correctifs urgents

Node.js a publié des mises à jour correctives pour 16 vulnérabilités affectant ses environnements d'exécution, dont sept sont classées comme critiques. Ces failles concernent principalement les implémentations intégrées des serveurs HTTP/2, HTTPS et TLS.

**Points clés :**
*   Les vulnérabilités permettent à des attaquants non authentifiés de faire planter les serveurs, d'accéder à des données sensibles en mémoire ou de provoquer des fuites d'informations entre connexions.
*   Les versions concernées sont les branches actives 22.x, 24.x et 26.x.
*   Les versions en fin de vie (EOL), telles que 20.x et 25.x, ne recevront aucun correctif et demeurent exposées.
*   Aucune solution de contournement n'a été identifiée ; la mise à jour est la seule mesure de protection.

**Vulnérabilités majeures identifiées :**
*   **CVE-2026-123863 :** Crash serveur via HTTP/2 (processus déclenché avant la réception complète du corps de la requête).
*   **CVE-2026-123866 :** Fuite de mémoire HTTP/2, exposant potentiellement des données destinées à d'autres connexions.
*   **CVE-2026-123864 :** Fuite de mémoire HTTPS (incluant des clés privées TLS et des requêtes d'utilisateurs).
*   **CVE-2026-123865 :** Épuisement des ressources (mémoire et descripteurs de fichiers) sur les serveurs HTTP/2.
*   **CVE-2026-123874 / CVE-2026-123875 :** Corruption de mémoire et plantage lors de la gestion de flux de fichiers.
*   **CVE-2026-126051 :** Crash serveur TLS via des hooks spécifiques (SNICallback, OCSPRequest, etc.).
*   **CVE-2026-123872 :** Contournement des règles de sécurité lors de la renégociation TLS 1.2.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs vers les versions **22.23.5**, **24.22.3** ou **26.13.1** selon votre branche.
*   **Migration :** Pour les systèmes utilisant des versions obsolètes (20.x, 25.x), une montée de version vers une branche supportée est impérative pour remédier à ces failles.
*   **Audit de sécurité :** Bien que non spécifié par l'avis, si une exposition liée à la faille HTTPS (CVE-2026-123864) est suspectée, il est prudent d'envisager la rotation des clés privées TLS et des secrets exposés.

---
[Source](https://thehackernews.com/2026/11/nodejs-fixes-16-flaws-including-http2.html){:target="_blank"}
