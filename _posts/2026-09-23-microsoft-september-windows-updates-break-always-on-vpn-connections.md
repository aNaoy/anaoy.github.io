---
title: 'Microsoft: September Windows updates break Always On VPN connections'
date: 2026-09-23
permalink: /posts/2026/09/23/microsoft-september-windows-updates-break-always-on-vpn-connections/
tags:
- veille-cyber
- bleepingcomp
---
### Instabilité des connexions Always On VPN après les mises à jour Windows de septembre 2026

Les mises à jour de sécurité cumulatives de septembre 2026 pour Windows 11 (KB5124012 et KB5124008) provoquent des dysfonctionnements majeurs sur les connexions « Always On VPN ». Ce problème survient principalement lorsque le profil VPN est configuré pour basculer automatiquement entre différents protocoles (IKEv2 et SSTP) en cas d'échec initial.

**Points clés :**
*   **Symptômes :** Les systèmes restent bloqués sur l'état « Connexion » ou tentent de se connecter en boucle sans succès.
*   **Erreur observée :** « Le port spécifié est déjà utilisé » (*The specified port is already in use*).
*   **Versions impactées :** Windows 11 versions 24H2, 25H2 et 26H1.
*   **Contexte :** Ce problème s'inscrit dans une série d'instabilités causées par les mises à jour de septembre, affectant également les services de bureau à distance (RDS), l'audio USB et l'historique des fichiers.

**Vulnérabilités :**
*   Aucune vulnérabilité CVE n'est associée à cet incident. Il s'agit d'une régression logicielle introduite par les correctifs de sécurité de Microsoft.

**Recommandations :**
*   En attendant un correctif permanent, les administrateurs informatiques doivent modifier les profils Always On VPN pour désactiver la sélection automatique des protocoles.
*   Forcer l'utilisation d'un protocole unique (soit IKEv2 uniquement, soit SSTP uniquement) selon les exigences spécifiques de l'environnement réseau.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-september-2026-windows-updates-break-always-on-vpn-connections/){:target="_blank"}
