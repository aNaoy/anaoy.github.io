---
title: 'Microsoft to retire the OWA Light client in Exchange Server'
date: 2026-07-09
permalink: /posts/2026/07/09/microsoft-to-retire-the-owa-light-client-in-exchange-server/
tags:
- veille-cyber
- bleepingcomp
---
### Retrait de la version OWA Light d'Exchange Server

Microsoft a annoncé la suppression prochaine de la version « Light » d'Outlook Web Access (OWA) dans Exchange Server. Introduite il y a vingt ans pour pallier les limitations des anciens navigateurs et des connexions à faible débit, cette interface est jugée obsolète face aux capacités des navigateurs modernes. Cette mesure vise à réduire la surface d'attaque « héritée » et à simplifier la maintenance technique.

**Points clés :**
* **Fin de support :** La suppression effective est prévue pour une mise à jour d'Exchange Server estimée à août 2026.
* **Modernisation :** Les utilisateurs devront migrer vers l'interface standard d'Outlook sur le web, qui offre des fonctionnalités complètes absentes de la version Light (calendriers partagés, gestion des tâches, etc.).
* **Surface d'attaque :** La suppression des fonctionnalités legacy permet de renforcer la posture de sécurité globale de l'infrastructure Exchange.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée à cette annonce. Toutefois, le maintien de composants logiciels obsolètes (« legacy surface area ») augmente structurellement le risque de vulnérabilités exploitables, justifiant cette mesure préventive.

**Recommandations pour les administrateurs :**
* **Désactivation anticipée :** Il est possible de désactiver dès maintenant OWA Light via PowerShell :
    * `Set-OwaMailboxPolicy -Identity <PolicyName> -OwaLightEnabled $false`
    * `Set-OwaVirtualDirectory -Identity <VirtualDirName> -LogonPageLightSelectionEnabled $false`
* **Accompagnement :** Préparer les utilisateurs finaux à la transition vers l'interface moderne d'Outlook sur le web avant la suppression définitive prévue en août 2026.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-announces-owa-light-retirement-in-exchange-server/){:target="_blank"}
