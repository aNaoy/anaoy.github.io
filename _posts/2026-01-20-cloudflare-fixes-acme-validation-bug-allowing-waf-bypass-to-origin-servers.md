---
title: 'Cloudflare Fixes ACME Validation Bug Allowing WAF Bypass to Origin Servers'
date: 2026-01-20
permalink: /posts/2026/01/20/cloudflare-fixes-acme-validation-bug-allowing-waf-bypass-to-origin-servers/
tags:
- veille-cyber
- hackernews
---
**Contournement du WAF Cloudflare via une faille ACME**

Une vulnérabilité dans la gestion des requêtes du protocole ACME par Cloudflare permettait de contourner le Web Application Firewall (WAF) et d'atteindre les serveurs d'origine. Cette faille exploitait la manière dont le système gérait les défis de validation du protocole ACME (HTTP-01).

**Points clés :**

*   **Protocole ACME :** Utilisé pour l'émission, le renouvellement et la révocation automatiques des certificats SSL/TLS. La validation se fait par des "défis" (challenges) pour prouver la propriété d'un domaine. Le défi HTTP-01 vérifie l'existence d'un jeton spécifique à une URL prédéfinie (`/.well-known/acme-challenge/*`).
*   **Fonctionnement initial :** Lorsque Cloudflare gérait un défi ACME pour un domaine, il désactivait le WAF pour éviter d'interférer avec le processus de validation.
*   **La faille :** Le système ne vérifiait pas systématiquement si le jeton de défi présent dans la requête correspondait à une commande active gérée par Cloudflare. Si le jeton était associé à une autre zone ou ne correspondait pas, la requête était transmise au serveur d'origine sans que le WAF ne bloque la requête.
*   **Conséquence :** Un attaquant pouvait envoyer des requêtes malveillantes sur ce chemin, potentiellement pour obtenir des jetons durables et accéder à des informations sensibles sur le serveur d'origine.
*   **Absence d'exploitation malveillante constatée :** Cloudflare n'a trouvé aucune preuve que cette vulnérabilité ait été exploitée dans un contexte malveillant.

**Vulnérabilités :**

*   Pas de CVE spécifique mentionné dans l'article. La vulnérabilité réside dans une mauvaise implémentation de la logique de validation des défis ACME HTTP-01, permettant un contournement du WAF.

**Recommandations :**

*   **Correction par Cloudflare :** La vulnérabilité a été corrigée le 27 octobre 2025 par une mise à jour du code. La désactivation du WAF et la transmission de la réponse ne se font désormais que si la requête correspond à un défi ACME HTTP-01 valide pour le nom d'hôte concerné.
*   **Pour les utilisateurs :** Il est conseillé de s'assurer que ses services Cloudflare sont à jour et de surveiller les annonces de sécurité. L'article suggère de suivre Cloudflare sur les réseaux sociaux pour plus d'informations.

---
[Source](https://thehackernews.com/2026/01/cloudflare-fixes-acme-validation-bug.html){:target="_blank"}
