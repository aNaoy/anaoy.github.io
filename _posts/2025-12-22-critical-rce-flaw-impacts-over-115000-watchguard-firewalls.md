---
title: 'Critical RCE flaw impacts over 115,000 WatchGuard firewalls'
date: 2025-12-22
permalink: /posts/2025/12/22/critical-rce-flaw-impacts-over-115000-watchguard-firewalls/
tags:
- veille-cyber
- bleepingcomp
---
**Faille Critique sur les Pare-feux WatchGuard : Exécution de Code à Distance**

Une faille de sécurité critique permettant l'exécution de code à distance (RCE) affecte plus de 115 000 appareils WatchGuard Firebox exposés sur Internet. Cette vulnérabilité, identifiée sous la référence **CVE-2025-14733**, touche les pare-feux exécutant Fireware OS dans les versions 11.x et ultérieures, 12.x et ultérieures, ainsi que 2025.1 jusqu'à la version 2025.1.3.

Les attaquants peuvent exploiter cette faille sans authentification, nécessitant peu de complexité et sans interaction utilisateur. L'exploitation réussie permet d'exécuter du code arbitraire à distance sur les appareils vulnérables. La vulnérabilité réside dans une erreur d'écriture hors limites au sein du processus "iked" du système d'exploitation. Elle est particulièrement préoccupante lorsqu'elle est configurée pour les VPN mobiles utilisateurs avec IKEv2 et les VPN de succursales utilisant IKEv2 avec un pair dynamique.

La CISA a ajouté cette vulnérabilité à son catalogue des vulnérabilités connues exploitées (KEV) et a ordonné aux agences fédérales américaines de la corriger rapidement. Des indicateurs de compromission et une solution de contournement temporaire ont été fournis par WatchGuard pour aider les entreprises qui ne peuvent pas appliquer immédiatement les correctifs.

**Points Clés :**

*   **Produit Affecté :** WatchGuard Firebox (Fireware OS)
*   **Nombre d'Appareils Exposés :** Plus de 115 000
*   **Type de Vulnérabilité :** Exécution de Code à Distance (RCE)
*   **Exploitation :** Activement exploitée dans la nature

**Vulnérabilité :**

*   **CVE :** CVE-2025-14733
*   **Description :** Vulnérabilité d'écriture hors limites dans le processus "iked" du système d'exploitation.
*   **Conditions d'Exploitation :** Nécessite une configuration pour les VPN IKEv2 (mobiles utilisateurs ou succursales avec pair dynamique).

**Recommandations :**

*   **Appliquer les Correctifs :** WatchGuard a publié des mises à jour de sécurité pour corriger cette vulnérabilité. Il est impératif de les installer sur tous les appareils Firebox concernés.
*   **Contournement Temporaire :** Pour les appareils qui ne peuvent pas être immédiatement patchés, il est recommandé de désactiver les BOVPN à pair dynamique, d'ajouter de nouvelles politiques de pare-feu et de désactiver les politiques système par défaut qui gèrent le trafic VPN.
*   **Surveillance et Investigation :** Les entreprises doivent utiliser les indicateurs de compromission fournis par WatchGuard pour identifier d'éventuelles activités malveillantes sur leurs appareils.
*   **Rotation des Secrets :** En cas de détection d'activité malveillante, il est conseillé de faire pivoter tous les secrets stockés localement sur les pare-feux vulnérables.
*   **Mise hors Service :** Si aucune mesure d'atténuation n'est disponible, il peut être nécessaire de cesser d'utiliser le produit.

---
[Source](https://www.bleepingcomputer.com/news/security/over-115-000-watchguard-firewalls-vulnerable-to-ongoing-rce-attacks/){:target="_blank"}
