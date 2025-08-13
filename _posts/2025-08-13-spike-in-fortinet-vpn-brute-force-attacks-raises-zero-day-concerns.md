---
title: 'Spike in Fortinet VPN brute-force attacks raises zero-day concerns'
date: 2025-08-13
permalink: /posts/2025/08/13/spike-in-fortinet-vpn-brute-force-attacks-raises-zero-day-concerns/
tags:
- veille-cyber
- bleepingcomp
---
### Pic de Tentatives d'Attaques par Force Brute sur les VPN Fortinet et Préoccupations Zéro-Day

Une augmentation significative des attaques par force brute a ciblé les SSL VPN de Fortinet, suivie d'un déplacement vers FortiManager. Ces actions sont considérées comme un indicateur d'exploitation future de vulnérabilités potentielles, y compris des vulnérabilités inconnues (zéro-day).

**Points Clés :**

*   Une campagne d'attaques par force brute a été détectée en deux vagues, les 3 et 5 août.
*   La première vague ciblait les SSL VPN de Fortinet, tandis que la seconde s'est concentrée sur FortiManager.
*   Des analyses de fingerprinting réseau ont relié l'activité à des environnements potentiellement réutilisés.
*   Des pics d'activité similaires ont historiquement précédé la divulgation de nouvelles vulnérabilités chez le même fournisseur dans environ 80% des cas.
*   Ces scans visent à identifier les points d'entrée exposés et à évaluer leur potentiel d'exploitation.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée directement dans l'article. L'inquiétude porte sur la possibilité de futures vulnérabilités "zéro-day" anticipées par ces campagnes de reconnaissance.

**Recommandations :**

*   Ne pas ignorer ces pics d'activité comme de simples tentatives d'exploitation de failles corrigées.
*   Les considérer comme des précurseurs potentiels de divulgations de vulnérabilités zéro-day.
*   Bloquer les adresses IP associées à ces attaques. Les adresses identifiées sont :
    *   31.206.51.194
    *   23.120.100.230
    *   96.67.212.83
    *   104.129.137.162
    *   118.97.151.34
    *   180.254.147.16
    *   20.207.197.237
    *   180.254.155.227
    *   185.77.225.174
    *   45.227.254.113
*   Renforcer les mesures de sécurité pour bloquer ces tentatives.
*   Augmenter la protection des connexions sur les appareils Fortinet.
*   Durcir l'accès externe autant que possible, en limitant l'accès aux plages d'adresses IP et aux VPN de confiance uniquement.

---
[Source](https://www.bleepingcomputer.com/news/security/spike-in-fortinet-vpn-brute-force-attacks-raises-zero-day-concerns/){:target="_blank"}
