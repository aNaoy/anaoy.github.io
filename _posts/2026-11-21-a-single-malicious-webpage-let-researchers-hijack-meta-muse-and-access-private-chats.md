---
title: 'A Single Malicious Webpage Let Researchers Hijack Meta Muse and Access Private Chats'
date: 2026-11-21
permalink: /posts/2026/11/21/a-single-malicious-webpage-let-researchers-hijack-meta-muse-and-access-private-chats/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique de l'agent IA Meta Muse

Des chercheurs de la firme NebuSec ont démontré qu'une simple page web malveillante pouvait compromettre l'agent IA Meta Muse, permettant d'exfiltrer des conversations privées, des mémoires stockées et des identifiants de comptes connectés sans aucune alerte utilisateur.

**Points clés :**
* **Fonctionnement de l'attaque :** L'agent accède à une page web malveillante qui exploite une faille dans le navigateur intégré de Muse.
* **Élévation de privilèges :** En enchaînant cette vulnérabilité avec une faille du noyau Linux, les attaquants ont pris le contrôle total de la machine cloud dédiée à l'utilisateur.
* **Contournement des protections :** L'attaque a neutralisé "Sentinel", la couche de sécurité conçue par Meta pour isoler l'agent des données sensibles (mots de passe, jetons, fichiers stockés).
* **Portée limitée :** L'exploitation est restée confinée à la machine virtuelle de l'utilisateur visé, sans compromettre l'infrastructure globale de Meta ou d'autres comptes.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais identifie deux vecteurs : une faille logicielle dans le **navigateur intégré** de Muse et une vulnérabilité au niveau du **noyau Linux** du conteneur cloud.

**Recommandations :**
* **Mises à jour :** L'équipe de sécurité de Meta a confirmé avoir corrigé l'ensemble des failles identifiées. Il est impératif pour les utilisateurs de s'assurer que leur application est à jour avec les derniers correctifs de sécurité fournis par l'éditeur.

---
[Source](https://thehackernews.com/2026/11/a-single-malicious-webpage-let.html){:target="_blank"}
