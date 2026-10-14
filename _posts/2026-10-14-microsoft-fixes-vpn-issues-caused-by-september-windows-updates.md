---
title: 'Microsoft fixes VPN issues caused by September Windows updates'
date: 2026-10-14
permalink: /posts/2026/10/14/microsoft-fixes-vpn-issues-caused-by-september-windows-updates/
tags:
- veille-cyber
- bleepingcomp
---
### Résolution des pannes Always On VPN sous Windows 11

Microsoft a déployé des correctifs pour résoudre un problème de connectivité affectant la solution *Always On VPN*, introduit par les mises à jour de sécurité de septembre 2026. Ce dysfonctionnement empêchait l'établissement de tunnels sécurisés lors de l'utilisation de la sélection automatique de protocole (IKEv2 et SSTP), laissant les connexions bloquées ou générant des erreurs de port déjà utilisé.

**Points clés :**
*   **Systèmes impactés :** Windows 11 (versions 24H2 et ultérieures).
*   **Origine du problème :** Un conflit lors de la tentative de basculement automatique entre les protocoles IKEv2 et SSTP.
*   **Correctifs :** Les mises à jour cumulatives **KB5127648** et **KB5127646** corrigent définitivement ce bug.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident de service ; il s'agit d'une régression logicielle fonctionnelle.

**Recommandations :**
*   **Application immédiate :** Installer les mises à jour cumulatives KB5127648 ou KB5127646.
*   **Solution de contournement temporaire :** Pour les administrateurs ne pouvant pas mettre à jour le système immédiatement, il est conseillé de forcer l'utilisation d'un protocole unique (soit SSTP, soit IKEv2) dans les profils *Always On VPN* au lieu de laisser la sélection automatique activée.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-vpn-issues-caused-by-september-windows-updates/){:target="_blank"}
