---
title: 'Cloudflare misconfiguration behind recent BGP route leak'
date: 2026-01-26
permalink: /posts/2026/01/26/cloudflare-misconfiguration-behind-recent-bgp-route-leak/
tags:
- veille-cyber
- bleepingcomp
---
## Fuite de routage BGP due à une mauvaise configuration de Cloudflare

Un incident de 25 minutes a affecté le trafic IPv6, causant congestion, pertes de paquets et environ 12 Gbps de trafic abandonné. Le système BGP, responsable du routage des données sur Internet, a été impacté par une erreur de configuration accidentelle sur un routeur Cloudflare.

Cette mauvaise configuration, visant initialement à empêcher la diffusion de préfixes IPv6 spécifiques, a rendu la politique d'exportation trop permissive. Elle a entraîné la redistribution de routes internes vers des pairs et fournisseurs externes, créant des "route leaks" de type 3 et 4 selon la norme RFC7908. Un "route leak" se produit lorsqu'un système autonome viole les politiques de routage "valley-free", introduisant des chemins de trafic non prévus et potentiellement instables, entraînant l'abandon du trafic par les réseaux qui ne peuvent pas le gérer. Bien que principalement un problème de fiabilité, de tels incidents peuvent avoir des implications de sécurité, facilitant l'interception de trafic.

Cloudflare a rapidement détecté et corrigé l'incident en annulant manuellement la configuration et en suspendant temporairement l'automatisation.

### Points Clés :

*   **Cause :** Mauvaise configuration d'une politique BGP sur un routeur Cloudflare.
*   **Conséquence :** Fuite de routage BGP affectant le trafic IPv6, causant congestion et pertes de trafic.
*   **Type de fuite :** Mélange de "route leaks" de type 3 et 4 (RFC7908).
*   **Durée :** 25 minutes.
*   **Impact :** Traffic abandonné, congestion, pertes de paquets.

### Vulnérabilités :

*   **Type de vulnérabilité :** Mauvaise configuration réseau (BGP).
*   **Absence de CVE spécifique :** Cet événement est une mauvaise configuration et non une vulnérabilité logicielle exploitée avec un identifiant CVE.

### Recommandations :

Cloudflare a proposé les mesures suivantes pour éviter la récurrence de tels incidents :

*   Ajout de protections plus strictes basées sur les communautés pour l'exportation des routes.
*   Mise en place de vérifications CI/CD pour détecter les erreurs de politique avant leur déploiement.
*   Amélioration des capacités de détection précoce des anomalies.
*   Validation selon la norme RFC 9234.
*   Promotion de l'adoption de la validation des itinéraires BGP (RPKI) et des Autorisations de Préfixes de Service (ASPA).

---
[Source](https://www.bleepingcomputer.com/news/security/cloudflare-misconfiguration-behind-recent-bgp-route-leak/){:target="_blank"}
