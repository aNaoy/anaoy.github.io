---
title: 'Microsoft says October updates didn’t actually fix VPN issues'
date: 2026-10-21
permalink: /posts/2026/10/21/microsoft-says-october-updates-didnt-actually-fix-vpn-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Erreur de Microsoft : Les problèmes de VPN sur Windows 11 persistent

Microsoft a admis avoir déclaré à tort comme résolu un bug affectant « Always On VPN » dans les mises à jour cumulatives d'octobre 2026. Ce problème, apparu avec les mises à jour de septembre, empêche l'établissement de connexions sécurisées sur Windows 11 (versions 24H2 et ultérieures) lorsque la sélection automatique de protocole est activée.

**Points clés :**
*   **Dysfonctionnement :** Les connexions VPN restent bloquées sur l'état « Connexion en cours » ou échouent, affichant parfois l'erreur « Le port spécifié est déjà utilisé ».
*   **Cause :** Le bug survient lors de l'utilisation de la sélection automatique ou du basculement automatique entre les protocoles IKEv2 et SSTP.
*   **Statut actuel :** Le problème est rétrogradé au statut « Atténué » en attendant un correctif définitif prévu pour les prochaines semaines.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, il s'agit d'un bug de fonctionnement logiciel et non d'une faille de sécurité exploitée.

**Recommandations :**
*   **Contournement temporaire :** Les administrateurs informatiques sont invités à désactiver la sélection automatique de protocole dans les profils « Always On VPN ».
*   **Configuration manuelle :** Forcer l'utilisation d'un seul protocole spécifique (soit SSTP uniquement, soit IKEv2 uniquement) en fonction des exigences de sécurité et de l'environnement de l'entreprise.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-didnt-actually-fix-vpn-issues-caused-by-windows-updates/){:target="_blank"}
