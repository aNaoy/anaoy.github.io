---
title: 'Quick notes on KERNSEAL'
date: 2026-03-25
permalink: /posts/2026/03/25/quick-notes-on-kernseal/
tags:
- veille-cyber
- zerodaysfans
---
### Présentation de KERNSEAL : Protection du noyau par auto-scellement mémoire

KERNSEAL est une technologie de protection du noyau Linux développée par l'équipe PaX, visant à empêcher l'élévation de privilèges en cas de lecture/écriture arbitraire en mémoire noyau. Contrairement aux approches basées sur le matériel, KERNSEAL utilise une isolation purement logicielle pour rendre inviolables des structures de données critiques.

**Points clés :**
*   **Constification dynamique :** KERNSEAL marque des objets noyau sensibles comme immuables (lecture seule) ou totalement inaccessibles (cachés) dans la mémoire physique directe.
*   **Gestion mémoire :** L'allocateur buddy est modifié pour grouper les pages « scellées » (`PG_sealed`) et « cachées » (`PG_hidden`) via de nouveaux types de migration non fusionnables.
*   **Accès temporaire :** Le noyau utilise des mécanismes de type `pax_expose_page` pour accéder temporairement aux données cachées lors d'opérations légitimes, garantissant que les accès non autorisés échouent.
*   **Application concrète :** La structure `struct cred` (gérant les privilèges) est scindée : les champs sensibles sont placés sur des pages scellées, tandis que les champs mutables (compteurs de références) restent en zone accessible.
*   **Indépendance matérielle :** La solution ne nécessite pas de fonctionnalités processeur spécifiques, ce qui la distingue des protections propriétaires comme celles d'Apple (PPL/SPTM).

**Dépendances de sécurité :**
Pour fonctionner, KERNSEAL exige l'activation de plusieurs autres protections PaX :
*   **RAP (Return Address Protection) :** Pour contrer l'exécution de code hors-ordre.
*   **PAX_PRIVATE_KSTACKS :** Pour isoler les piles d'exécution par CPU.
*   **CONFIG_PAX_PER_CPU_PGD :** Pour empêcher les accès inter-CPU aux pages non scellées.
*   **Isolation des tables de pages (KPTI) :** Protection standard contre les fuites.
*   **Restrictions :** Absence de support pour l'hibernation et `kexec`.

**Recommandations :**
*   **Déploiement :** Intégrer KERNSEAL dans les environnements à haute exigence de sécurité où le risque d'exploitation de vulnérabilités mémoire (ex: corruption de `struct cred`) est critique.
*   **Surveillance :** Utiliser les nouveaux compteurs fournis dans `/proc/meminfo` et `/proc/<pid>/smaps` pour surveiller l'état des pages scellées et cachées.
*   **Débogage :** En cas d'erreur `BUG()` lors d'un accès mémoire, vérifier le diagnostic fourni par le gestionnaire de page fault, qui précise désormais si la page fautive était scellée ou cachée.

*Note : KERNSEAL est actuellement disponible pour les clients bêta et LTS de grsecurity.*

---
[Source](https://dustri.org/b/quick-notes-on-kernseal.html){:target="_blank"}
