---
title: 'Microsoft Xbox One Hacked'
date: 2026-03-23
permalink: /posts/2026/03/23/microsoft-xbox-one-hacked/
tags:
- veille-cyber
- schneier
---
### Compromission matérielle de la Xbox One : L'exploit "Bliss"

Plus de dix ans après sa sortie, la Xbox One a été intégralement compromise via une attaque matérielle sophistiquée baptisée « Bliss ». En utilisant une technique de *voltage glitching* (injection de fautes par variation de tension) visant le processeur, le chercheur a réussi à contourner les protections du processeur ARM Cortex et à injecter du code non signé au niveau du démarrage.

**Points clés :**
* **Nature de l'attaque :** Attaque matérielle ciblant la ROM de démarrage (*boot ROM*) via deux glitches de tension successifs.
* **Impact :** Compromission totale du système, incluant l'hyperviseur et le système d'exploitation. 
* **Accès aux données :** L'exploit permet d'accéder au processeur de sécurité, autorisant le déchiffrement des jeux et du firmware.
* **Persistance :** S'agissant d'une vulnérabilité liée au silicium, le défaut est inhérent au matériel et ne peut être corrigé par une mise à jour logicielle.

**Vulnérabilités :**
* Aucune CVE n'est attribuée à cette faille, car il s'agit d'une vulnérabilité matérielle physique non corrigeable (*unpatchable*) plutôt que d'un bug logiciel classique.

**Recommandations :**
* Aucune mesure corrective logicielle n'est possible pour les consoles existantes. Les propriétaires doivent être conscients que l'intégrité de la chaîne de confiance matérielle de ces appareils est désormais définitivement compromise.

---
[Source](https://www.schneier.com/blog/archives/2026/03/microsoft-xbox-hacked.html){:target="_blank"}
