---
title: 'Critical OpenWrt DHCPv6 Flaw Could Let Unauthenticated Attackers Run Code as Root'
date: 2026-07-28
permalink: /posts/2026/07/28/critical-openwrt-dhcpv6-flaw-could-let-unauthenticated-attackers-run-code-as-root/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans OpenWrt : Risque d'exécution de code à distance

OpenWrt a publié les versions 24.10.8 et 25.12.5 pour corriger une vulnérabilité critique affectant son service DHCPv6 (`odhcpd`). Cette faille permet à un attaquant non authentifié d'exécuter du code arbitraire avec les privilèges `root` sur les appareils cibles.

**Points clés :**
*   **CVE-2026-53921 (Score CVSS 9.8) :** Il s'agit d'un dépassement de mémoire tampon (stack overflow) déclenchable par l'envoi de paquets DHCPv6 malveillants (`REQUEST`) sur le port UDP 547.
*   **Gravité accrue :** L'absence fréquente de protections mémoires (ASLR et canaris de pile) sur le matériel embarqué facilite l'exploitation pour obtenir un contrôle total du routeur.
*   **Audit Hacker House :** Une série de vulnérabilités supplémentaires (injection de commandes, traversée de répertoire, XSS) a été découverte dans les composants optionnels de l'interface LuCI. Certaines sont en attente de correction.
*   **Autres vulnérabilités :** La mise à jour traite également une injection de nom d'hôte via DHCPv6 (CVE-2026-62948) et une faille de traversée de chemin dans `cgi-io` (CVE-2026-62947).

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions 24.10.8 ou 25.12.5 via le sélecteur de firmware OpenWrt.
*   **Gestion des paquets :** Mettre à jour les paquets installés indépendamment du firmware.
*   **Audit de configuration :** 
    *   Supprimer les applications LuCI optionnelles inutilisées.
    *   Vérifier les permissions dans `luci-app-commands` : s'assurer qu'aucune commande paramétrée n'est configurée comme "publique" (`public=1`).
*   **Migration :** Envisager la migration vers la branche 25.12, la version 24.10 arrivant en fin de vie en septembre 2026.

---
[Source](https://thehackernews.com/2026/07/critical-openwrt-dhcpv6-flaw-could-let.html){:target="_blank"}
