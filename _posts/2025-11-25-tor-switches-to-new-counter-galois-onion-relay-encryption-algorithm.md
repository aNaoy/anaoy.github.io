---
title: 'Tor switches to new Counter Galois Onion relay encryption algorithm'
date: 2025-11-25
permalink: /posts/2025/11/25/tor-switches-to-new-counter-galois-onion-relay-encryption-algorithm/
tags:
- veille-cyber
- bleepingcomp
---
### Tor Renforce sa Sécurité avec le Nouvel Algorithme CGO

Le réseau Tor adopte un nouvel algorithme de chiffrement, le Counter Galois Onion (CGO), remplaçant l'ancien système tor1. Cette mise à jour vise à renforcer la sécurité du trafic des circuits Tor face aux attaques modernes de brouillage de données et à améliorer l'anonymat des utilisateurs. Le réseau Tor, connu pour son anonymat et sa capacité à contourner la censure, est utilisé par une diversité d'individus, allant des militants aux cybercriminels.

Les faiblesses du protocole tor1, développé à une époque où la cryptographie était moins avancée, sont désormais corrigées. Celles-ci incluent une vulnérabilité à des attaques permettant la modification du trafic par des relais compromis, un manque de confidentialité persistante (forward secrecy) due à la réutilisation des clés de chiffrement, et une authentification de cellule faible utilisant SHA-1 avec une probabilité de falsification significative.

Le nouvel algorithme CGO, basé sur la construction RPRP UIV+ et des recherches cryptographiques, apporte plusieurs améliorations clés :

**Points Clés :**

*   **Robustesse accrue contre les attaques :** Le CGO résiste aux tentatives de modification du trafic.
*   **Confidentialité persistante améliorée :** Les clés sont mises à jour après chaque paquet, protégeant les communications passées même en cas de compromission des clés actuelles.
*   **Authentification renforcée :** L'utilisation de SHA-1 est abandonnée au profit d'un authentificateur plus sûr de 16 octets.
*   **Intégrité des circuits :** Chaque paquet dépend des précédents, rendant les falsifications plus difficiles à dissimuler.

Ces améliorations sont conçues sans impacter significativement la bande passante. Le déploiement du CGO est en cours dans les implémentations C de Tor et Arti, et la fonctionnalité est actuellement marquée comme expérimentale. Aucune date n'a été spécifiée pour son activation par défaut.

**Vulnérabilités corrigées (sans CVEs spécifiques mentionnés pour ces faiblesses générales du tor1) :**

*   **Malleabilité du chiffrement de relais :** Permettant des attaques par modification de trafic (type "tagging attack").
*   **Confidentialité persistante partielle :** Réutilisation des clés AES tout au long d'un circuit, permettant le déchiffrement en cas de vol de clé.
*   **Authentification faible des cellules :** Utilisation de SHA-1 pour la validation des cellules, offrant une faible résistance à la falsification (probabilité de 1 sur 4 milliards).

**Recommandations / Améliorations apportées par CGO :**

*   Protection contre les attaques par marquage ("tagging").
*   Confidentialité immédiate et persistante ("forward secrecy").
*   Tags d'authentification plus longs.
*   Utilisation d'une cryptographie modernisée.
*   Suppression de SHA-1 pour l'authentification.
*   Chiffrement large bloc et chaînage de tags pour assurer l'intégrité.
*   Mise à jour des clés après chaque cellule.

---
[Source](https://www.bleepingcomputer.com/news/security/tor-switches-to-new-counter-galois-onion-relay-encryption-algorithm/){:target="_blank"}
