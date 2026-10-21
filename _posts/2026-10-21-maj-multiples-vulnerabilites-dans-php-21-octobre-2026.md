---
title: '[Màj] Multiples vulnérabilités dans PHP (21 octobre 2026)'
date: 2026-10-21
permalink: /posts/2026/10/21/maj-multiples-vulnerabilites-dans-php-21-octobre-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilités critiques dans PHP : Risque d'exécution de code à distance

PHP a corrigé deux vulnérabilités majeures permettant à un attaquant d'exécuter du code arbitraire à distance (RCE). Les versions 5.x, 6.x, 7.x, 8.0.x et 8.1.x, bien que non supportées par l'éditeur, sont également exposées.

**Points clés :**
*   **Vulnérabilités :** CVE-2026-109618 et CVE-2026-109619.
*   **Impact :** Exécution de code arbitraire à distance.
*   **Disponibilité :** Les correctifs de sécurité officiels sont disponibles auprès de l'éditeur depuis le 21 octobre 2026.

**Recommandations :**
*   **Migration :** Mettre à jour immédiatement vers une version de PHP maintenue et appliquer les derniers correctifs.
*   **Isolement :** Isoler les équipements affectés en attendant leur mise à jour.
*   **Atténuations temporaires (WAF/Configuration) :**
    *   Désactiver la fonctionnalité `session.upload_progress` dans `php.ini` (`session.upload_progress.enabled = Off`) et, si nécessaire, dans `php-fpm`.
    *   Bloquer ou superviser strictement les requêtes HTTP contenant l'en-tête `Content-Type: multipart` via un pare-feu applicatif (WAF).
    *   *Note : Ces mesures sont partielles et ne garantissent pas une protection complète contre les deux vulnérabilités.*

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-014/){:target="_blank"}
