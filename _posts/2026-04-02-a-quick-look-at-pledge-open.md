---
title: 'A quick look at __pledge_open'
date: 2026-04-02
permalink: /posts/2026/04/02/a-quick-look-at-pledge-open/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse de `__pledge_open(2)` dans OpenBSD 7.9-beta

L'introduction de l'appel système `__pledge_open(2)` dans OpenBSD 7.9-beta marque une évolution dans la gestion des permissions des processus. Cet appel est exclusivement réservé à la bibliothèque standard (`libc`) et permet d'ouvrir certains fichiers ou périphériques spécifiques (comme `/etc/resolv.conf`, `/etc/localtime` ou `/dev/null`) sans nécessiter les promesses `rpath` ou `wpath` habituelles.

**Points clés :**
*   **Contournement restreint :** Bien que `__pledge_open(2)` ignore les restrictions `pledge` et `unveil`, son usage est strictement limité par le noyau à une liste prédéfinie de chemins et de conditions associées aux promesses (`dns`, `stdio`, `tty`, `getpw`).
*   **Protection :** L'appel est protégé par le mécanisme `pinsyscall`, empêchant son exécution directe depuis l'espace utilisateur en dehors de la `libc`.
*   **Sandbox :** L'analyse montre que le système de fichiers `pledge` effectue des vérifications rigoureuses (`pledge_namei`) pour valider les chemins demandés, rendant une exploitation malveillante complexe, voire impossible dans les configurations standards.

**Vulnérabilités :**
*   Aucune vulnérabilité directe n'est exploitée. Une tentative de contournement via un appel direct à la fonction dans la `libc` échoue, car le noyau valide le chemin et le contexte de la promesse avant d'autoriser l'accès.
*   **Cas particulier :** Une vulnérabilité potentielle pourrait subsister uniquement dans les noyaux compilés avec l'option `SMALL_KERNEL` (utilisée pour économiser de la RAM), où les vérifications des chemins sont simplifiées et font confiance aveuglément aux requêtes provenant de la `libc`.

**Recommandations :**
*   **Éviter `SMALL_KERNEL` :** Pour les systèmes nécessitant un haut niveau de sécurité, il est recommandé d'utiliser des noyaux complets qui appliquent l'ensemble des vérifications `pledge_namei` sur les chemins accédés via `__pledge_open`.
*   **Intégrité de la libc :** Étant donné que `__pledge_open` est un pont privilégié vers le noyau, la sécurité repose sur l'impossibilité d'exécuter ce code arbitrairement ; veillez à ce que les mécanismes de protection contre le détournement de flux de contrôle restent activés.

---
[Source](https://dustri.org/b/a-quick-look-at-__pledge_open2.html){:target="_blank"}
