---
title: 'Microsoft: Teams increasingly abused in helpdesk impersonation attacks'
date: 2026-04-20
permalink: /posts/2026/04/20/microsoft-teams-increasingly-abused-in-helpdesk-impersonation-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Usurpation d'identité via Microsoft Teams : une menace persistante

Les attaquants exploitent de plus en plus la collaboration externe via Microsoft Teams pour se faire passer pour du personnel de support informatique. En manipulant les employés pour obtenir un accès à distance, les cybercriminels s'introduisent dans les réseaux d'entreprise, utilisant des outils légitimes pour mener leurs activités malveillantes sans éveiller les soupçons.

**Points clés :**
*   **Mode opératoire :** Utilisation de chats externes Teams pour inciter les victimes à lancer une session de contrôle à distance (ex: Quick Assist).
*   **Persistance et furtivité :** L'attaque s'appuie sur des applications légitimes signées (via *DLL side-loading*) et des protocoles d'administration natifs (WinRM), rendant l'activité difficile à distinguer des opérations IT normales.
*   **Exfiltration :** Utilisation de l'utilitaire Rclone pour transférer sélectivement des données sensibles vers des services de stockage cloud.
*   **Vulnérabilités :** L'article ne mentionne aucune CVE spécifique ; les attaquants tirent profit de l'utilisation détournée d'outils d'administration légitimes et de l'ingénierie sociale.

**Recommandations :**
*   **Sensibilisation :** Considérer par défaut toute communication Teams provenant d'un contact externe comme suspecte et porter une attention particulière aux avertissements de sécurité natifs de Microsoft.
*   **Gestion des accès :** Restreindre strictement l'usage des outils d'assistance à distance et limiter l'accès via WinRM uniquement aux systèmes contrôlés.
*   **Surveillance :** Surveiller étroitement l'utilisation des outils de gestion à distance et les comportements anormaux sur le réseau, même lorsqu'ils semblent provenir d'applications autorisées.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-teams-increasingly-abused-in-helpdesk-impersonation-attacks/){:target="_blank"}
