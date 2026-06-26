---
title: 'Polymarket customers lose $3 million in supply-chain attack'
date: 2026-06-26
permalink: /posts/2026/06/26/polymarket-customers-lose-3-million-in-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par chaîne d'approvisionnement chez Polymarket : 3 millions de dollars dérobés

La plateforme de prédictions cryptographiques Polymarket a été victime d'une attaque par chaîne d'approvisionnement (supply-chain attack) ayant conduit au vol d'environ 3 millions de dollars auprès de ses utilisateurs. Bien que les serveurs internes et l'infrastructure backend de l'entreprise soient restés sécurisés, l'injection d'un script malveillant via un fournisseur tiers a compromis le frontend du site.

**Points clés :**
*   **Nature de l'attaque :** Injection de code JavaScript malveillant via une dépendance externe sur le frontend.
*   **Impact financier :** Environ 3 millions de dollars dérobés (convertis en 1 893 ETH).
*   **Victimes :** Un nombre limité d'utilisateurs (moins de 15 comptes affectés).
*   **Réaction :** Polymarket s'est engagé à rembourser intégralement les clients impactés.

**Vulnérabilités :**
*   **Vulnérabilité de la chaîne d'approvisionnement :** L'incident souligne la dépendance critique aux bibliothèques ou services tiers. Aucune CVE spécifique n'a été associée à cette intrusion, le vecteur étant une compromission directe du fournisseur externe.

**Recommandations :**
*   **Audit des dépendances :** Réaliser un inventaire rigoureux de toutes les bibliothèques tierces intégrées au frontend et limiter les privilèges accordés à ces scripts.
*   **Mise en œuvre d'une CSP (Content Security Policy) :** Renforcer la politique de sécurité du contenu pour restreindre l'exécution de scripts provenant de sources non autorisées.
*   **Subresource Integrity (SRI) :** Utiliser l'intégrité des sous-ressources pour vérifier que les fichiers chargés depuis des serveurs tiers n'ont pas été altérés.
*   **Surveillance proactive :** Surveiller les comportements anormaux sur les interfaces utilisateurs pour détecter rapidement toute injection de script non sollicité.

---
[Source](https://www.bleepingcomputer.com/news/security/polymarket-customers-lose-3-million-in-supply-chain-attack/){:target="_blank"}
