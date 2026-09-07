---
title: 'N-able patches max severity N-central flaw amid ongoing attacks'
date: 2026-09-07
permalink: /posts/2026/09/07/n-able-patches-max-severity-n-central-flaw-amid-ongoing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Alerte de sécurité critique sur la plateforme N-able N-central

N-able a publié un correctif d'urgence pour sa plateforme de gestion et de surveillance (RMM) N-central, visant une vulnérabilité critique d'exécution de code à distance (RCE). Cette faille, activement surveillée par les experts en cybersécurité, permet à des attaquants non authentifiés de compromettre des instances exposées en ligne avec une grande facilité.

**Points clés :**
*   **Risque majeur :** La vulnérabilité permet une exécution de code à distance sans privilèges requis.
*   **Exposition :** Près de 1 500 serveurs N-central sont actuellement accessibles via Internet, principalement aux États-Unis et en Europe.
*   **Exploitation potentielle :** Bien que N-able n'ait pas confirmé d'exploitation généralisée, Huntress soupçonne une utilisation active par des attaquants, couplée à deux autres failles d'authentification récemment corrigées.

**Vulnérabilités identifiées :**
*   **CVE-2026-86218 :** Faille RCE de sévérité maximale (nécessite le déploiement du Hotfix 4).
*   **CVE-2026-86206 et CVE-2026-86207 :** Vulnérabilités de haute sévérité permettant le contournement de l'authentification (corrigées dans le Hotfix 3).

**Recommandations :**
*   **Mise à jour immédiate :** Les clients utilisant des déploiements sur site doivent impérativement installer **N-central 2026.3 Hotfix 4**.
*   **Vérification :** Le passage au Hotfix 3 est insuffisant ; seule l'application du Hotfix 4 permet de neutraliser la faille CVE-2026-86218.
*   **Surveillance :** Inspecter les journaux des serveurs exposés pour détecter toute activité suspecte, en gardant à l'esprit que la rotation des logs peut masquer des tentatives d'intrusion passées.

---
[Source](https://www.bleepingcomputer.com/news/security/n-able-patches-max-severity-n-central-flaw-amid-ongoing-attacks/){:target="_blank"}
