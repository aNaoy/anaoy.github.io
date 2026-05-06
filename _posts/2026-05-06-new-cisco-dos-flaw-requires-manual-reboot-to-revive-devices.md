---
title: 'New Cisco DoS flaw requires manual reboot to revive devices'
date: 2026-05-06
permalink: /posts/2026/05/06/new-cisco-dos-flaw-requires-manual-reboot-to-revive-devices/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité DoS critique sur Cisco CNC et NSO

Cisco a publié des mises à jour correctives pour remédier à une vulnérabilité de déni de service (DoS) affectant ses solutions *Crosswork Network Controller* (CNC) et *Network Services Orchestrator* (NSO).

**Points clés :**
*   La faille permet à un attaquant non authentifié de saturer les ressources de connexion à distance, rendant le système totalement inopérant.
*   Le rétablissement des services nécessite une intervention manuelle (redémarrage physique du système).
*   Bien qu'aucune exploitation active ne soit signalée à ce jour, la sévérité de la faille impose une action rapide.

**Vulnérabilité :**
*   **CVE-2026-20188** : Faille de haute sévérité due à une gestion insuffisante du débit (rate limiting) des connexions réseau entrantes.

**Recommandations :**
*   **Mise à jour immédiate :** Cisco recommande vivement de migrer vers les versions logicielles corrigées.
    *   **Cisco CNC :** Migrer les versions 7.1 et antérieures vers une version corrigée (7.2 n'est pas vulnérable).
    *   **Cisco NSO :** Pour la branche 6.4, passer à la version 6.4.1.3 ou ultérieure. Les versions 6.3 et antérieures doivent être mises à jour (6.5 n'est pas vulnérable).

---
[Source](https://www.bleepingcomputer.com/news/security/new-cisco-dos-flaw-requires-manual-reboot-to-revive-devices/){:target="_blank"}
