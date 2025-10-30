---
title: 'X-Request-Purpose: Identifying "research" and bug bounty related scans&#x3f;, (Thu, Oct 30th)'
date: 2025-10-30
permalink: /posts/2025/10/30/x-request-purpose-identifying-research-and-bug-bounty-related-scansx3f-thu-oct-30th/
tags:
- veille-cyber
- sans-isc
---
## Identification des requêtes de bug bounty

Certaines entreprises intègrent l'utilisation d'en-têtes HTTP spécifiques lors de campagnes de bug bounty. Ces en-têtes, tels que `X-Request-Purpose: Research`, `X-Hackerone-Research: plusultra`, `X-Bugcrowd-Ninja: plusultra` ou encore `X-Bug-Hunter: true`, servent à identifier les requêtes comme provenant de chercheurs en sécurité participant à ces programmes.

Bien que leur présence dans des honeypots puisse sembler inhabituelle, elle peut s'expliquer si ces honeypots font partie de réseaux d'entreprises inclus dans le périmètre d'un bug bounty. L'utilisation de ces en-têtes vise à faciliter la communication entre l'entreprise et le chercheur en cas de problème causé par les scans.

Du point de vue de la défense, il est conseillé de ne pas traiter ces requêtes différemment des autres. Bloquer ou autoriser ces requêtes sur la seule base de leur en-tête spécifique n'est pas pertinent. La décision doit se fonder sur le reste de la requête.

Il est également recommandé aux sites web de mettre en place un fichier `/.well-known/security.txt` pour améliorer la gestion de la sécurité.

**Points clés:**

*   Des en-têtes HTTP spécifiques sont utilisés pour identifier les requêtes issues de programmes de bug bounty.
*   Ces en-têtes facilitent la communication entre entreprises et chercheurs.
*   Il est préférable de ne pas traiter ces requêtes de manière distincte des autres.

**Vulnérabilités:**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans le texte.

**Recommandations:**

*   Ne pas traiter les requêtes avec ces en-têtes différemment des autres requêtes.
*   Mettre en place un fichier `/.well-known/security.txt`.

---
[Source](https://isc.sans.edu/diary/rss/32436){:target="_blank"}
