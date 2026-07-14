---
title: 'Progress confirms ShareFile zero-day flaw behind Storage Zone shutdown'
date: 2026-07-14
permalink: /posts/2026/07/14/progress-confirms-sharefile-zero-day-flaw-behind-storage-zone-shutdown/
tags:
- veille-cyber
- bleepingcomp
---
### Correction de la faille critique dans ShareFile Storage Zone Controller

Progress Software a identifié une vulnérabilité « zero-day » de haute gravité affectant les contrôleurs de zones de stockage (Storage Zone Controllers) de ShareFile, suite à une alerte concernant une menace externe crédible. Bien que l'accès aux serveurs ait été temporairement coupé par précaution, l'entreprise affirme qu'aucune preuve d'exploitation active ou d'accès non autorisé aux données clients n'a été détectée à ce jour.

**Points clés :**
*   **Produit concerné :** ShareFile Storage Zone Controller (versions 5.x et 6.x).
*   **Nature de la menace :** Une faille de type « path traversal » permettant à un utilisateur administrateur authentifié de lire des fichiers arbitraires, d'écrire du contenu malveillant ou d'énumérer le système de fichiers du serveur.
*   **Statut CVE :** Un identifiant CVE est réservé et sera rendu public d'ici deux semaines.

**Recommandations :**
*   **Mise à jour immédiate :** Les administrateurs doivent installer sans délai les versions corrigées **5.12.5** ou **6.0.2**.
*   **Rétablissement de service :** Les serveurs peuvent être remis en ligne une fois les correctifs appliqués.

---
[Source](https://www.bleepingcomputer.com/news/security/progress-confirms-sharefile-zero-day-flaw-behind-storage-zone-shutdown/){:target="_blank"}
