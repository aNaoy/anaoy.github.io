---
title: 'HollowByte DDoS flaw bloats OpenSSL server memory with 11-byte payload'
date: 2026-07-17
permalink: /posts/2026/07/17/hollowbyte-ddos-flaw-bloats-openssl-server-memory-with-11-byte-payload/
tags:
- veille-cyber
- bleepingcomp
---
### HollowByte : Vulnérabilité DoS par épuisement mémoire dans OpenSSL

La vulnérabilité **HollowByte** permet à un attaquant non authentifié de provoquer une saturation de la mémoire vive (DoS) sur les serveurs utilisant OpenSSL, en envoyant des requêtes malveillantes de seulement 11 octets.

**Points clés :**
* **Mécanisme d'attaque :** Lors d'un handshake TLS, OpenSSL alloue de la mémoire en se basant uniquement sur la taille déclarée dans l'en-tête du paquet (4 octets) avant même de vérifier la réception effective des données.
* **Fragmentation mémoire :** En multipliant les connexions avec des tailles déclarées aléatoires, l'attaquant empêche le gestionnaire de mémoire (`glibc`) de réutiliser les buffers libérés, provoquant une fragmentation intense et une augmentation permanente de l'empreinte mémoire du serveur (RSS).
* **Impact opérationnel :** Le serveur peut perdre jusqu'à 25 % de sa mémoire vive avec un très faible volume de données envoyées, rendant l'attaque difficile à détecter par les seuils de trafic classiques. La libération de la mémoire ne peut être obtenue qu'en redémarrant le processus.

**Vulnérabilités :**
* Aucune référence CVE n'a été attribuée par l'équipe OpenSSL, la correction ayant été traitée comme une mesure de "durcissement" (hardening).

**Recommandations :**
* **Mise à jour immédiate :** Mettre à jour les paquets OpenSSL vers les versions corrigées. Les correctifs sont inclus dans les versions **4.0.1, 3.6.3, 3.5.7, 3.4.6 et 3.0.21**.
* **Approche :** La nouvelle version modifie le comportement du serveur pour qu'il n'alloue le buffer qu'à la réception effective des données, ignorant les déclarations de taille contenues dans les en-têtes.

---
[Source](https://www.bleepingcomputer.com/news/security/hollowbyte-ddos-flaw-bloats-openssl-server-memory-with-11-byte-payload/){:target="_blank"}
