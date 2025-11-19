---
title: 'W3 Total Cache WordPress plugin vulnerable to PHP command injection'
date: 2025-11-19
permalink: /posts/2025/11/19/w3-total-cache-wordpress-plugin-vulnerable-to-php-command-injection/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité Critique dans W3 Total Cache pour WordPress**

Une faille de sécurité majeure a été découverte dans le plugin W3 Total Cache (W3TC) pour WordPress, permettant l'exécution de commandes PHP arbitraires sur le serveur. Cette vulnérabilité, identifiée sous la référence CVE-2025-9501, affecte toutes les versions antérieures à la version 2.8.13 du plugin et ne nécessite aucune authentification pour être exploitée.

L'exploitation de cette faille se fait en soumettant un commentaire malveillant à un article. Les attaquants peuvent ainsi prendre le contrôle total d'un site WordPress vulnérable en exécutant n'importe quelle commande sur le serveur. Un exemple de code (Proof-of-Concept) pour cette vulnérabilité a été développé et sera publié prochainement.

**Points Clés :**

*   **Nature de la faille :** Injection de commande PHP (PHP Command Injection).
*   **Impact :** Prise de contrôle totale du site WordPress, exécution de commandes serveur sans authentification.
*   **Mode d'exploitation :** Soumission d'un commentaire malveillant contenant une charge utile.

**Vulnérabilité :**

*   **CVE-2025-9501**

**Recommandations :**

*   **Mettre à jour immédiatement** le plugin W3 Total Cache vers la version 2.8.13 ou supérieure.
*   En cas d'impossibilité de mise à jour, il est conseillé de **désactiver temporairement le plugin W3 Total Cache**.
*   Une autre mesure consiste à **empêcher l'envoi de commentaires malveillants** pouvant déclencher l'exploit.

---
[Source](https://www.bleepingcomputer.com/news/security/w3-total-cache-wordpress-plugin-vulnerable-to-php-command-injection/){:target="_blank"}
