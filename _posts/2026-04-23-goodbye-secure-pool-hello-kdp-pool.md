---
title: 'Goodbye Secure Pool, Hello KDP Pool'
date: 2026-04-23
permalink: /posts/2026/04/23/goodbye-secure-pool-hello-kdp-pool/
tags:
- veille-cyber
- zerodaysfans
---
### Évolution de la sécurité noyau Windows : Du Secure Pool au KDP Pool

Microsoft a introduit dans Windows 11 (version 26H2) une évolution majeure de ses mécanismes de protection des données critiques. Le "Secure Pool" (ou Dynamic KDP), autrefois utilisé par des chercheurs pour identifier des vulnérabilités, a été supprimé au profit d'une nouvelle implémentation plus flexible et sécurisée : le **KDP Pool**.

#### Fonctionnement technique
Le KDP Pool repose sur l'utilisation d'une section dédiée du noyau nommée `KDPRO`. Son mécanisme de protection s'articule autour de deux axes :
*   **Allocation initiale :** Lors de la phase 1 du démarrage du noyau, les données sensibles (variables statiques et données dynamiques via `ExKdproPoolAllocate`) sont écrites dans la section `KDPRO`.
*   **Verrouillage par l'hyperviseur :** Une fois l'initialisation terminée, le noyau invoque des appels sécurisés (`SECURESERVICE_REGISTER_PROTECTED_PAGE` et `SECURESERVICE_PROTECT_KERNEL_DATA_PAGE`) pour demander au noyau sécurisé de marquer ces pages en lecture seule via SLAT (Second Level Address Translation).

#### Objectifs de sécurité
Cette protection vise à contrer les attaques par **écriture arbitraire en mode noyau**. En rendant immuables des structures critiques, Windows empêche un attaquant de modifier les privilèges ou les contrôles d'accès pour élever ses droits. Les données protégées incluent :
*   **Privilèges :** Variables comme `SeDebugPrivilege` (pour éviter l'usurpation de capacités debug).
*   **Identifiants et accès :** SIDs bien connus, DACLs par défaut, et ACEs.

#### Points clés
*   **Protection renforcée :** Même un attaquant disposant de droits d'écriture en mode noyau (Ring 0) ne peut plus modifier les données dans `KDPRO` car la protection est gérée au niveau de l'hyperviseur (VTL1).
*   **Absence de randomisation :** Contrairement aux pools classiques, le KDP Pool est séquentiel. Cette simplicité est justifiée par le fait qu'il est exclusivement rempli lors du démarrage et ne permet aucune libération mémoire (`free`) par la suite, limitant la surface d'attaque.
*   **Limite actuelle :** La taille de la section est limitée à 0x1000 octets.
*   **Réplication possible :** Bien qu'il s'agisse d'une fonctionnalité interne à `ntoskrnl.exe`, sa conception ne repose pas sur de nouvelles fonctionnalités hyperviseur, permettant potentiellement aux développeurs de pilotes de reproduire un mécanisme similaire pour leurs propres données sensibles.

#### Recommandations
*   **Pour les chercheurs :** Étant donné que le KDP Pool protège des données de sécurité cruciales, l'analyse des vecteurs d'attaque doit désormais se concentrer sur les composants qui ne sont pas encore migrés vers `KDPRO` (ex: les jetons/tokens de processus ou certaines descripteurs de sécurité WMI/ETW).
*   **Pour les développeurs :** Il est conseillé de migrer les constantes de sécurité et les variables de configuration critiques vers ce modèle de protection en lecture seule pour minimiser l'impact potentiel d'une vulnérabilité d'écriture arbitraire.

---
[Source](https://windows-internals.com/goodbye-secure-pool-hello-kdp-pool/?utm_source=rss&utm_medium=rss&utm_campaign=goodbye-secure-pool-hello-kdp-pool){:target="_blank"}
