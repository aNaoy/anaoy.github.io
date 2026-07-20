---
title: 'Microsoft confirms Windows Server Update Services sync delays'
date: 2026-07-20
permalink: /posts/2026/07/20/microsoft-confirms-windows-server-update-services-sync-delays/
tags:
- veille-cyber
- bleepingcomp
---
### Perturbation des services de synchronisation WSUS

Microsoft a confirmé l'existence de problèmes techniques affectant les serveurs WSUS (*Windows Server Update Services*), entraînant des échecs de synchronisation ou des délais d'expiration lors de la récupération des métadonnées de mise à jour. Cette anomalie impacte l'ensemble des systèmes clients (Windows 10 et versions ultérieures) et serveurs (Windows Server 2012 et ultérieurs).

**Points clés :**
* **Nature du problème :** La synchronisation entre les serveurs WSUS locaux et les serveurs de mise à jour de Microsoft est interrompue ou ralentie, empêchant le déploiement efficace des mises à jour sur les réseaux d'entreprise.
* **Historique :** Ce dysfonctionnement fait suite à une série de problèmes récurrents rencontrés sur WSUS au cours des 18 derniers mois.
* **Vulnérabilités :** Aucune CVE n'est associée à cet incident, il s'agit d'un problème de disponibilité et de fonctionnement opérationnel des services et non d'une faille de sécurité exploitable.

**Recommandations :**
* **Nouvelles installations :** Le service est opérationnel pour les nouveaux serveurs WSUS ou les réinstallations, suite aux mesures d'atténuation déployées par Microsoft.
* **Serveurs existants :** Pour les serveurs déjà impactés, Microsoft travaille actuellement sur des procédures spécifiques permettant de nettoyer les métadonnées corrompues. Il est conseillé aux administrateurs réseau de surveiller les bulletins d'état de santé de Windows (*Windows Health Dashboard*) pour obtenir les prochaines instructions de remédiation technique.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-working-to-fix-wsus-server-sync-delays-and-timeouts/){:target="_blank"}
