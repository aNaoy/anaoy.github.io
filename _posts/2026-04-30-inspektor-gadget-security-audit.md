---
title: 'Inspektor Gadget Security Audit'
date: 2026-04-30
permalink: /posts/2026/04/30/inspektor-gadget-security-audit/
tags:
- veille-cyber
- zerodaysfans
---
### Audit de sécurité : Inspektor Gadget

Shielder, mandaté par l'OSTIF, a réalisé un audit de sécurité approfondi d'Inspektor Gadget, un framework d'observabilité basé sur l'eBPF pour Kubernetes et Linux. L'analyse a combiné des tests dynamiques, une revue de code (SAST) et une modélisation des menaces.

#### Vulnérabilités identifiées
*   **Injection de commande dans `ig build` :** L'utilisation de Makefiles pour la construction des gadgets permettait une injection de commandes si les variables étaient manipulées. *Corrigé en v0.51.1 par une refonte en Go.*
*   **Déni de service (DoS) par saturation :** Le remplissage délibéré du buffer d'événements (256 Ko) permettait de saturer le système et d'occulter des activités malveillantes. *Corrigé par la mise en place d'une détection de perte de paquets.*
*   **Injection de séquences ANSI :** L'absence de nettoyage des séquences d'échappement dans les logs pouvait permettre à un attaquant de manipuler l'affichage du terminal. *Corrigé par une sanitisation des sorties.*

#### Recommandations de sécurité
*   **Sécurisation par défaut :** Activer systématiquement le TLS sur les écouteurs TCP (`ig daemon`).
*   **Gestion de la Supply Chain :** Épingler les dépendances par hash au lieu d'utiliser des tags comme `latest` pour prévenir les attaques sur la chaîne de compilation.
*   **Isolation Kubernetes :** Implémenter une liste d'exclusion (blocklist) des espaces de noms sensibles pour limiter le périmètre de tracing.
*   **Gestion des permissions :** Remplacer la permission critique `GET nodes/proxy` par un mécanisme de bootstrap plus restreint.
*   **Audit continu :** Intégrer des outils de scan de dépendances (ex: `osv-scanner`) dans le pipeline CI/CD.

#### Limites et contournements (Bypasses)
L'audit a révélé plusieurs méthodes permettant d'échapper à la surveillance d'Inspektor Gadget, notamment :
*   Utilisation d'appels système alternatifs récents (`openat2`, API `fs*`).
*   Exploitation de protocoles ou formats réseau non surveillés (Jumbo frames, IPv6 pour le SNI).
*   Liaison statique des bibliothèques pour contourner les hooks `uprobe`.
*   Abus de l'API `io_uring` pour exécuter des syscalls non tracés.

**Conclusion :** Bien que des techniques d'évasion existent, Inspektor Gadget reste un outil précieux pour l'observabilité. Il doit cependant être intégré dans une stratégie de défense en profondeur, en gardant à l'esprit que les capacités de tracing ne sont pas infaillibles face à un attaquant déterminé ayant un accès privilégié.

---
[Source](https://www.shielder.com/blog/2026/04/inspektor-gadget-security-audit/){:target="_blank"}
