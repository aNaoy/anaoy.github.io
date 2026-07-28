---
title: 'New Dysphoria DDoS botnet spreads to 200k devices worldwide'
date: 2026-07-28
permalink: /posts/2026/07/28/new-dysphoria-ddos-botnet-spreads-to-200k-devices-worldwide/
tags:
- veille-cyber
- bleepingcomp
---
### Expansion et menaces du botnet Dysphoria

Le botnet **Dysphoria** a compromis environ 200 000 appareils IoT (routeurs, caméras, etc.) à travers le monde. Évoluant à partir des familles *jackskid* et *fbot*, ce réseau se distingue par une architecture de commande et contrôle (C2) hautement résiliente basée sur la blockchain (Ethereum ENS et Solana SNS) et des algorithmes de masquage sophistiqués. Il est principalement utilisé pour des attaques DDoS (capacité revendiquée de 4 Tbps) et des opérations de relais réseau par proxy.

**Points clés :**
*   **Infrastructure C2 :** Utilisation de domaines décentralisés et dissimulation des adresses dans de fausses chaînes IPv6.
*   **Fonctionnalités :** Support multi-chaîne, séparation des rôles entre bots DDoS et bots-proxys, et abus du protocole UPnP pour l'exposition de services internes.
*   **Propagation :** Exploitation de vulnérabilités connues dans les équipements IoT et usage de mots de passe par défaut (Telnet/SSH).

**Vulnérabilités exploitées :**
*   **Récentes :** CVE-2025-55182 (React2Shell), CVE-2025-34152, CVE-2025-28137, CVE-2025-9528.
*   **Anciennes :** CVE-2017-17215 (Huawei) et CVE-2020-8515 (DrayTek).

**Recommandations :**
*   **Mises à jour :** Appliquer systématiquement les correctifs de firmware pour combler les failles de sécurité.
*   **Gestion des accès :** Remplacer les identifiants par défaut par des mots de passe robustes.
*   **Durcissement réseau :** Désactiver l'accès distant non nécessaire et désactiver le protocole UPnP sur les routeurs pour limiter l'exposition.

---
[Source](https://www.bleepingcomputer.com/news/security/new-dysphoria-ddos-botnet-spreads-to-200k-devices-worldwide/){:target="_blank"}
