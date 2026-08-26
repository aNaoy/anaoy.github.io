---
title: 'New SLEEPWALKER Backdoor Waits for One Crafted Packet, Then Runs Its Own Bytecode'
date: 2026-08-26
permalink: /posts/2026/08/26/new-sleepwalker-backdoor-waits-for-one-crafted-packet-then-runs-its-own-bytecode/
tags:
- veille-cyber
- hackernews
---
### Analyse du logiciel malveillant SLEEPWALKER

**Points clés :**
* **Nature :** SLEEPWALKER est un *backdoor* passif pour Windows, conçu pour rester inactif en mémoire jusqu'à la réception d'un paquet réseau spécifique (« magic packet »).
* **Fonctionnement :** Il exécute un bytecode personnalisé (23 instructions) et utilise six vecteurs de transport, incluant TCP, UDP, ICMP, SMB, et l'interface VMCI de VMware.
* **Persistance :** Il utilise le détournement de DLL (*DLL side-loading*) en se faisant passer pour `dpapi.dll` au sein du processus `ERAAgent.exe` (ESET Management Agent).
* **Discrétion :** Le malware n'effectue aucune connexion sortante et ne contient aucune adresse IP ou nom de domaine en dur, ce qui le rend invisible pour les outils de surveillance réseau classiques.
* **Contexte :** Il s'agit d'un outil de post-compromission nécessitant des droits d'administrateur local pour être déployé.

**Vulnérabilités :**
* Aucune CVE n'est associée. La compromission repose sur le **DLL search order hijacking** (détournement de l'ordre de recherche des DLL de Windows), une faiblesse architecturale plutôt qu'une faille logicielle spécifique dans ESET.

**Indicateurs de compromission (IoC) :**
* Présence de fichiers `dpapi.dll` ou `dpapisvc.dll` suspects dans le répertoire d'ESET.
* Modification des clés de registre : `EveryoneIncludesAnonymous` définie à 1 et ajout d'entrées suspectes dans `NullSessionPipes`.
* Empreintes numériques (Hash SHA-256) : `d347170752a28e2b8c4b8b9f3cab2e3a6541ba11682c94498d26eb9002779d60`.

**Recommandations :**
* **Audit :** Comparer les répertoires d'installation d'ESET Management Agent avec une base de référence saine pour détecter les DLL intruses.
* **Surveillance :** Surveiller les changements dans le registre (`NullSessionPipes` et `EveryoneIncludesAnonymous`) qui facilitent les mouvements latéraux non authentifiés.
* **Réponse à incident :** Étant donné le mode de persistance, la recommandation en cas d'infection confirmée est la reconstruction complète du système compromis, après avoir neutralisé le vecteur d'accès initial.
* **Détection :** Utiliser des règles YARA basées sur les signatures binaires connues pour identifier des variantes potentielles.

---
[Source](https://thehackernews.com/2026/08/newly-sleepwalker-backdoor-waits-for.html){:target="_blank"}
