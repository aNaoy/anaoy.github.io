---
title: 'How has use of framing protection security headers changed in the past 3 years&#x3f;, (Wed, Jun 10th)'
date: 2026-06-10
permalink: /posts/2026/06/10/how-has-use-of-framing-protection-security-headers-changed-in-the-past-3-yearsx3f-wed-jun-10th/
tags:
- veille-cyber
- sans-isc
---
### État des lieux de la protection contre le détournement de clic (Clickjacking)

L'étude compare l'utilisation des en-têtes de sécurité `X-Frame-Options` et `Content-Security-Policy (CSP) : frame-ancestors` sur le million de domaines les plus populaires entre 2023 et 2026. Ces en-têtes sont essentiels pour empêcher le "framing" malveillant, technique utilisée dans les attaques de phishing par superposition (overlay phishing).

**Points clés :**
*   **Progression globale :** Le taux d'adoption de ces protections a nettement augmenté sur l'ensemble du million de domaines (passant de 14,4 % à 29,7 %).
*   **Supériorité du CSP :** Bien que `X-Frame-Options` reste largement utilisé (notamment l'option `SAMEORIGIN`), la directive `frame-ancestors` du CSP est désormais privilégiée car plus flexible et moderne.
*   **Évolution des pratiques :** On observe une augmentation de l'utilisation de `frame-ancestors 'none'`, indiquant une volonté croissante des administrateurs d'interdire strictement toute mise en iframe de leurs contenus.
*   **Paradoxe des leaders :** Le top 1 000 des sites a paradoxalement vu sa couverture diminuer, probablement en raison de la nature technique des nouveaux domaines entrants (CDN, API, infrastructures) qui ne nécessitent pas de rendu HTML traditionnel.

**Vulnérabilités :**
*   L'absence de ces en-têtes expose les utilisateurs aux attaques par **"overlay phishing"**, où un attaquant charge une page légitime dans une iframe invisible ou superposée pour tromper l'utilisateur.
*   *Note :* Il n'existe pas de CVE spécifique, car il s'agit d'une configuration de sécurité côté serveur et non d'une faille logicielle native.

**Recommandations :**
1.  **Privilégier le CSP :** Utiliser la directive `frame-ancestors` comme protection principale, car elle est plus robuste et largement supportée par les navigateurs modernes.
2.  **Maintenir la compatibilité :** Continuer à envoyer l'en-tête `X-Frame-Options` pour assurer la protection des navigateurs plus anciens, bien qu'il soit ignoré par les navigateurs modernes si une règle CSP est présente.
3.  **Implémentation simple :** L'ajout de ces en-têtes via la configuration du serveur (ex: Nginx, Apache) est une opération triviale et hautement efficace pour sécuriser une application web.

---
[Source](https://isc.sans.edu/diary/rss/33068){:target="_blank"}
