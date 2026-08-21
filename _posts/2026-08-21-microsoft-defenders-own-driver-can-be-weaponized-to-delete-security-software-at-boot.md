---
title: 'Microsoft Defenders Own Driver Can Be Weaponized to Delete Security Software at Boot'
date: 2026-08-21
permalink: /posts/2026/08/21/microsoft-defenders-own-driver-can-be-weaponized-to-delete-security-software-at-boot/
tags:
- veille-cyber
- hackernews
---
### Détournement du pilote de remédiation de Microsoft Defender : Une menace persistante

Des chercheurs de Check Point Research ont découvert qu'il est possible de détourner `BTR.sys`, un pilote légitime signé par Microsoft utilisé par Defender pour la remédiation au démarrage. Cette technique permet à un attaquant disposant de privilèges administratifs d'effectuer des opérations arbitraires au niveau du noyau (Kernel), notamment la suppression ou la modification de fichiers protégés et de clés de registre.

**Points clés :**
* **Fonctionnement :** Le pilote `BTR.sys` est extrait de `MpEngine.dll`. L'attaquant utilise un protocole de transaction RC4 chiffré (clé statique) pour manipuler le pilote, lui ordonnant de supprimer des logiciels de sécurité lors de la phase de démarrage critique ("golden window"), avant que les protections de Windows ne soient actives.
* **Absence de faille logicielle :** Il ne s'agit pas d'une vulnérabilité classique (type buffer overflow), mais d'une exploitation architecturale. Le pilote étant un composant système essentiel, il ne peut être ajouté à la liste de blocage des pilotes vulnérables sans compromettre la stabilité de Defender.
* **Contournement des traces :** L'installation du pilote via des écritures directes dans le registre permet de contourner le gestionnaire de services Windows (Service Control Manager), évitant ainsi la génération de l'événement classique d'installation de service (ID 7045).

**Vulnérabilités :**
* Aucune CVE associée (problème de conception architecturale).
* Prérequis : Nécessite des privilèges d'administrateur avec le droit `SeLoadDriverPrivilege`.

**Recommandations :**
* **Durcissement :** Restreindre strictement l'attribution du privilège `SeLoadDriverPrivilege` aux seuls utilisateurs autorisés.
* **Détection :** Surveiller via Sysmon les indicateurs suivants :
    * ID 15 : Création de flux de données alternatifs (ADS) nommés `.sys:changelist`.
    * ID 12/13 : Création de clés de service avec le groupe "Boot Bus Extender" sans événement 7045 associé.
    * ID 11/23 : Activité de lecture/écriture du fichier `\SystemRoot\Temp\BootClean.log` par le processus système (PID 4).
    * ID 6 : Chargement de pilote suivi immédiatement d'une suppression de fichier par le processus système.

---
[Source](https://thehackernews.com/2026/08/microsoft-defenders-own-driver-can-be.html){:target="_blank"}
