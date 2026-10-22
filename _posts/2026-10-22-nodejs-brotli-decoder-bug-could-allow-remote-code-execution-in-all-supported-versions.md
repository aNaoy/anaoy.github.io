---
title: 'Node.js Brotli Decoder Bug Could Allow Remote Code Execution in All Supported Versions'
date: 2026-10-22
permalink: /posts/2026/10/22/nodejs-brotli-decoder-bug-could-allow-remote-code-execution-in-all-supported-versions/
tags:
- veille-cyber
- hackernews
---
### Mise à jour de sécurité critique pour Node.js : Correction de 10 vulnérabilités

Node.js a publié des mises à jour correctives pour les versions 22.x, 24.x et 26.x afin de résoudre dix vulnérabilités, dont une faille critique dans le décodeur Brotli susceptible d'entraîner une exécution de code à distance (RCE).

**Points clés :**
*   **Faille Brotli (CVE-2026-111497) :** Un dépassement de tampon (out-of-bounds write) dans le décodeur Brotli peut être déclenché par une entrée compressée malformée. Bien que classée "haute" sévérité, l'exploitation réelle sur des configurations standard est complexe.
*   **Autres vulnérabilités :** Les correctifs incluent des contournements de vérification TLS, des erreurs de troncature de noms d'hôte DNS et des problèmes de prédictibilité dans les fonctions de cryptographie (`randomUUID`/`randomInt`).
*   **Certificats compromis :** Node.js bloque désormais huit clés d'autorité de certification intermédiaires (eMudhra) suite à leur compromission.
*   **Dépendances :** Mise à jour des composants intégrés, notamment `undici` (client HTTP), `c-ares`, OpenSSL et SQLite.

**Vulnérabilités majeures (CVE) :**
*   **CVE-2026-111497 :** Exécution de code via le décodeur Brotli.
*   **CVE-2026-106069 / CVE-2026-105483 :** Contournement des contrôles d'hôte TLS.
*   **CVE-2026-105482 :** Troncature de noms d'hôte via octet nul dans `dns.resolve`.

**Recommandations :**
*   **Mettre à jour immédiatement :** Migrer vers les versions corrigées : **22.23.4**, **24.22.1** ou **26.12.1**.
*   **Abandonner les versions obsolètes :** Les versions 20.x et antérieures ne sont plus supportées et ne recevront pas ces correctifs ; une migration vers une version active est indispensable.
*   **Vérification des dépendances :** Étant donné que la faille Brotli concerne une bibliothèque partagée, assurez-vous que les autres logiciels utilisant Brotli sont également mis à jour vers les versions 1.2.1, 1.1.1 ou 1.0.10.
*   **Absence de contournement :** Aucun workaround interne n'est disponible pour la faille Brotli ; la mise à jour logicielle est la seule solution viable.

---
[Source](https://thehackernews.com/2026/10/nodejs-brotli-decoder-bug-could-allow.html){:target="_blank"}
