---
title: 'Critical vm2 Node.js Flaw Allows Sandbox Escape and Arbitrary Code Execution'
date: 2026-01-28
permalink: /posts/2026/01/28/critical-vm2-nodejs-flaw-allows-sandbox-escape-and-arbitrary-code-execution/
tags:
- veille-cyber
- hackernews
---
### Grave vulnérabilité dans vm2 : Évasion du bac à sable et exécution de code arbitraire

Une faille critique dans la bibliothèque Node.js vm2 permet aux attaquants de s'échapper de l'environnement sécurisé (bac à sable) et d'exécuter du code arbitraire sur le système d'exploitation sous-jacent.

**Points Clés:**

*   La vulnérabilité est causée par un **assainissement insuffisant des gestionnaires de Promise** dans la bibliothèque vm2.
*   Les fonctions asynchrones JavaScript renvoient des objets `globalPromise` plutôt que des `localPromise`. Les méthodes `then` et `catch` de `globalPromise` n'étant pas correctement assainies, cela crée une voie d'évasion du bac à sable.
*   Bien que ce ne soit pas la première vulnérabilité de ce type affectant vm2, elle est qualifiée de critique avec un score CVSS de 9.8/10.
*   Le projet vm2 a été précédemment annoncé comme étant discontinué, mais les versions 3.x sont activement maintenues. Cependant, de nouvelles contournements sont anticipés.

**Vulnérabilité:**

*   **CVE-2026-22709**: Permet l'évasion du bac à sable et l'exécution de code arbitraire par le biais d'une mauvaise gestion des `Promise.prototype.then` et `Promise.prototype.catch`.

**Recommandations:**

*   **Mettre à jour vers la dernière version :** La version 3.10.3 de vm2 corrige cette vulnérabilité, ainsi que d'autres failles d'évasion de bac à sable.
*   **Envisager des alternatives plus robustes :** Pour des garanties d'isolation plus solides, des bibliothèques comme `isolated-vm` sont recommandées.
*   **Maintenir une isolation stricte :** Il est conseillé d'utiliser des solutions comme Docker pour une séparation logique des composants, même avec des outils d'isolation.

---
[Source](https://thehackernews.com/2026/01/critical-vm2-nodejs-flaw-allows-sandbox.html){:target="_blank"}
