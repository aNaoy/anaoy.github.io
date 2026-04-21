---
title: 'Hooking Windows Named Pipes'
date: 2026-04-21
permalink: /posts/2026/04/21/hooking-windows-named-pipes/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse et exploitation des Windows Named Pipes

Les Named Pipes constituent un mécanisme de communication inter-processus (IPC) couramment utilisé sous Windows pour échanger des données entre des processus de privilèges différents (ex: un processus utilisateur communiquant avec un service SYSTEM). Leur architecture partagée et leur configuration par défaut en font des vecteurs d'attaque privilégiés pour des scénarios de type *Man-in-the-Middle* (MitM).

#### Points clés
*   **Fonctionnement :** Les pipes sont référencés dans `\.\pipe\` et reposent sur des APIs système (`CreateNamedPipe`, `NtCreateNamedPipeFile`, `CreateFile`).
*   **Instances :** Un pipe peut posséder plusieurs instances ; la première connexion client est liée à la première instance disponible.
*   **Interception :** Il est possible d'intercepter, modifier ou injecter des données dans les flux de communication en utilisant des techniques de *hooking* (ex: via Frida) sur les appels système de lecture/écriture, qu'ils soient synchrones, asynchrones, basés sur des ports de complétion ou des routines de complétion.

#### Vulnérabilités
*   **Permissive ACLs :** Par défaut, les permissions accordées sur les Named Pipes (via les ACL) peuvent être trop larges, permettant à un utilisateur non privilégié de créer ses propres instances de pipe et d'intercepter le trafic destiné à un processus privilégié.
*   **Défaut de contrainte de création :** L'absence de verrouillage sur la création de la première instance de pipe permet à un attaquant de "devancer" le processus légitime (race condition) en créant le pipe avec des permissions permissives avant lui.

#### Recommandations
*   **Durcissement des ACL :** Appliquer des listes de contrôle d'accès (ACL) restrictives lors de la création du pipe, en évitant d'accorder des droits de type `FILE_APPEND_DATA` aux utilisateurs non autorisés.
*   **Flag de sécurité :** Utiliser systématiquement l'option `FILE_FLAG_FIRST_PIPE_INSTANCE` lors de l'appel à `CreateNamedPipe`. Cela garantit que la création échouera si une instance malveillante a déjà été créée par un tiers, empêchant ainsi le détournement.
*   **Validation des données :** Ne jamais faire confiance aux données reçues via les pipes ; toute information provenant d'un canal IPC doit être traitée comme non fiable et rigoureusement validée.
*   **Vérification des pairs :** Bien que non infaillibles, le contrôle de la signature numérique du processus distant ou de son PID peut renforcer la sécurité globale, bien que cela ne remplace pas une protection rigoureuse des accès au pipe.

---
[Source](https://www.synacktiv.com/en/publications/hooking-windows-named-pipes){:target="_blank"}
