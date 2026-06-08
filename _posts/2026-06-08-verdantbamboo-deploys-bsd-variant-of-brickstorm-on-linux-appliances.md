---
title: 'VerdantBamboo Deploys BSD Variant of BRICKSTORM on Linux Appliances'
date: 2026-06-08
permalink: /posts/2026/06/08/verdantbamboo-deploys-bsd-variant-of-brickstorm-on-linux-appliances/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage de VerdantBamboo ciblant les appliances Linux

Le groupe d'espionnage informatique lié à la Chine, **VerdantBamboo** (connu sous d'autres noms comme Clay Typhoon ou UNC5221), mène des attaques sophistiquées en ciblant des appliances réseau et de stockage Linux, souvent dépourvues de solutions EDR. Les attaquants compromettent des Managed Services Providers (MSP) pour infiltrer leurs clients via des accès VPN SSL et des privilèges administratifs volés.

**Points clés :**
*   **Tactiques :** Utilisation de techniques "living-off-the-land" et déploiement de malwares personnalisés pour maintenir la persistance.
*   **Objectifs :** Accès aux environnements cloud (Microsoft 365) en contournant les politiques d'accès conditionnel.
*   **Arsenal :**
    *   **BRICKSTORM :** Backdoor multiplateforme (incluant une variante BSD pour pare-feu pfSense).
    *   **PLENET (GRIMBOLT) :** Backdoor en .NET Core permettant le contrôle distant, l'exécution de commandes et la manipulation de fichiers.
    *   **AGENTPSD :** Reverse shell en Python agissant comme secours.

**Vulnérabilités :**
*   **CVE-2026-22769 (Score CVSS 10.0) :** Exploitation d'une vulnérabilité zero-day dans *Dell RecoverPoint for Virtual Machines* (utilisée par des groupes liés).
*   **Escalade de privilèges locale :** Identifiée dans le système *Egnyte Storage Sync* (corrigée en version 13.13).

**Recommandations :**
*   **Mise à jour :** Appliquer immédiatement les correctifs pour les appliances de stockage (ex: Egnyte Storage Sync) et les solutions de virtualisation.
*   **Sécurisation des accès :** Renforcer l'authentification des accès distants (VPN SSL) et surveiller de près les accès administratifs provenant des MSP.
*   **Visibilité :** Étendre la surveillance de sécurité au-delà des serveurs traditionnels pour inclure les appliances réseau (NAS, pare-feu), souvent négligées par les outils de protection classiques.
*   **Gestion des accès :** Réviser régulièrement les politiques d'accès conditionnel et les privilèges accordés aux comptes tiers/MSP.

---
[Source](https://thehackernews.com/2026/06/verdantbamboo-deploys-bsd-variant-of.html){:target="_blank"}
