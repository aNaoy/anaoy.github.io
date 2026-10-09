---
title: 'GoBalance Flaw Lets Attackers Hijack .onion Addresses by Recovering Tor-Format Keys'
date: 2026-10-09
permalink: /posts/2026/10/09/gobalance-flaw-lets-attackers-hijack-onion-addresses-by-recovering-tor-format-keys/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans GoBalance : Risque de détournement d'adresses .onion

Une faille de sécurité identifiée dans l'outil **GoBalance** (une implémentation en Go de l'équilibreur de charge *Onionbalance*) permet à des attaquants de récupérer la clé privée maîtresse de services cachés sur le réseau Tor. Cette compromission facilite le détournement complet d'adresses .onion, permettant aux attaquants de rediriger les utilisateurs vers des sites frauduleux sans pour autant accéder aux serveurs ou aux bases de données des victimes.

**Points clés :**
*   **Mécanisme de l'attaque :** GoBalance tronque par erreur la clé privée Ed25519 (64 octets) lors de la signature des descripteurs, ne conservant que les 32 premiers octets. Cette troncature rend la partie secrète du calcul de signature prévisible, permettant la reconstruction de la clé maîtresse à partir d'un simple descripteur public.
*   **Impact :** L'attaque permet de usurper durablement l'identité d'un service .onion. Des sites majeurs du dark web, tels que le forum *Dread* et le marché *Omega*, ont été contraints de changer d'adresse après des détournements constatés.
*   **Vulnérabilité :** Il n'existe actuellement aucun identifiant CVE officiel pour cette faille.
*   **Limitation :** Seuls les sites utilisant GoBalance et stockant leurs clés dans le format natif de Tor sont vulnérables. Les clés générées via l'outil de configuration de GoBalance (utilisant un format différent) ne sont pas affectées.

**Recommandations :**
*   **Pour les opérateurs de services :** Si une version vulnérable de GoBalance a été utilisée, la clé privée doit être considérée comme compromise. Il est impératif de générer une nouvelle adresse .onion et de migrer l'ensemble du service. Un correctif communautaire est disponible sur GitHub, mais il ne résout pas la compromission des clés déjà exposées.
*   **Pour les utilisateurs :** En cas de suspicion de compromission d'un service, il est recommandé de modifier immédiatement son mot de passe sur le site concerné ainsi que sur tout autre service réutilisant les mêmes identifiants. Il convient de vérifier l'authenticité des nouvelles adresses via des canaux de communication officiels signés.

---
[Source](https://thehackernews.com/2026/10/gobalance-flaw-lets-attackers-hijack.html){:target="_blank"}
