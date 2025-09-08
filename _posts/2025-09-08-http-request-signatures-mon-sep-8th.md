---
title: 'HTTP Request Signatures, (Mon, Sep 8th)'
date: 2025-09-08
permalink: /posts/2025/09/08/http-request-signatures-mon-sep-8th/
tags:
- veille-cyber
- sans-isc
---
**Authentification Renforcée des Requêtes HTTP par Signatures**

Une nouvelle technique, les signatures de messages HTTP (standardisées par RFC 9421), vise à améliorer l'authentification des requêtes, notamment celles provenant de robots. Traditionnellement, les robots s'identifient via des en-têtes `User-Agent`. Cependant, cette méthode peut être contournée, par exemple en utilisant le `User-Agent` de Googlebot pour accéder à du contenu payant. Bien que des mesures comme la résolution inverse des noms d'hôte pour les adresses IP de Google existent, elles ne sont pas toujours efficaces dans les architectures modernes où les adresses IP d'origine peuvent être masquées ou peu fiables.

Les signatures de messages HTTP introduisent trois nouveaux en-têtes : `Signature-Input`, `Signature-Agent` et `Signature`.

*   **`Signature-Agent`**: Ce champ spécifie une URL où le serveur peut récupérer la clé publique nécessaire à la vérification. Le fichier retourné est généralement au format JSON et contient la clé cryptographique (par exemple, Ed25519).
*   **`Signature-Input`**: Il définit les éléments de la requête qui sont inclus dans la signature (par exemple, l'autorité de la requête et l'en-tête `Signature-Agent`). Il inclut également des métadonnées telles que l'horodatage de création, la date d'expiration, l'identifiant de la clé (`keyid`), l'algorithme de signature (`alg`), un nonce et une description de l'usage de la clé (`tag`).
*   **`Signature`**: Cet en-tête contient la valeur de la signature calculée sur les éléments spécifiés dans `Signature-Input`.

Les serveurs peuvent ainsi récupérer les clés publiques des robots de confiance et n'accepter que les requêtes authentifiées par une signature valide. Des solutions comme Cloudflare et Zuplo intègrent déjà cette fonctionnalité.

**Points Clés :**

*   Les signatures de messages HTTP résolvent le problème de l'usurpation d'identité des robots.
*   Elles utilisent des clés publiques pour authentifier les requêtes.
*   Les en-têtes `Signature-Input`, `Signature-Agent` et `Signature` sont essentiels au fonctionnement.

**Vulnérabilités Adressées :**

*   Contournement des restrictions basées sur l'en-tête `User-Agent`.
*   Faiblesses de l'authentification basée sur les adresses IP dans les architectures modernes.
*   (Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article).

**Recommandations :**

*   Les serveurs devraient implémenter la validation des signatures de messages HTTP pour les requêtes de robots.
*   Les administrateurs peuvent définir des listes de confiance pour les clés publiques des robots.
*   Il est recommandé de consulter les implémentations et les guides disponibles (par exemple, Cloudflare, Zuplo) pour une mise en œuvre correcte.

---
[Source](https://isc.sans.edu/diary/rss/32266){:target="_blank"}
