---
title: 'New "Bad Epoll" Linux Kernel Flaw Lets Unprivileged Users Gain Root, Hits Android'
date: 2026-07-04
permalink: /posts/2026/07/04/new-bad-epoll-linux-kernel-flaw-lets-unprivileged-users-gain-root-hits-android/
tags:
- veille-cyber
- hackernews
---
### Bad Epoll : Une faille d'escalade de privilèges critique dans le noyau Linux

Une nouvelle vulnérabilité, baptisée **Bad Epoll**, permet à un utilisateur non privilégié d'obtenir les droits "root" sur les systèmes Linux et Android. Cette faille réside dans le sous-système `epoll`, un composant essentiel de gestion des événements réseau et de fichiers présent dans tous les environnements Linux.

#### Points clés
*   **Nature de la faille :** Il s'agit d'une vulnérabilité de type *use-after-free* (utilisation après libération) causée par une condition de compétition (*race condition*) lors de la gestion d'objets internes du noyau.
*   **Exploitation :** Bien que la fenêtre d'opportunité soit extrêmement étroite (environ six instructions machine), le chercheur Jaeyoung Chung a réussi à concevoir un exploit capable d'atteindre le niveau root avec un taux de réussite de 99 %.
*   **Contexte :** La faille peut être déclenchée depuis l'intérieur du sandbox de rendu de Google Chrome et affecte également Android. Elle est apparue suite à une modification du code en 2023 et n'a pas été détectée par l'intelligence artificielle qui avait pourtant identifié une faille similaire dans le même segment de code.

#### Vulnérabilité
*   **CVE-2026-46242** (Bad Epoll)

#### Recommandations
*   **Mise à jour :** Appliquer le correctif officiel disponible via le commit amont `a6dc643c6931`.
*   **Distribution :** Installer les mises à jour de sécurité fournies par votre distribution Linux dès qu'elles deviennent disponibles.
*   **Compatibilité :** Les noyaux Linux à partir de la version 6.4 sont vulnérables, sauf s'ils ont été patchés. Les versions antérieures (comme celles basées sur le noyau 6.1, présentes sur certains terminaux Android) ne sont pas affectées.
*   **Contournement :** Il n'existe aucun contournement possible, car `epoll` est un composant système indispensable qui ne peut être désactivé.

---
[Source](https://thehackernews.com/2026/07/new-bad-epoll-linux-kernel-flaw-lets.html){:target="_blank"}
