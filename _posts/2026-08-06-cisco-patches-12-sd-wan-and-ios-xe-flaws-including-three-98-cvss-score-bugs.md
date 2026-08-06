---
title: 'Cisco Patches 12 SD-WAN and IOS XE Flaws, Including Three 9.8 CVSS Score Bugs'
date: 2026-08-06
permalink: /posts/2026/08/06/cisco-patches-12-sd-wan-and-ios-xe-flaws-including-three-98-cvss-score-bugs/
tags:
- veille-cyber
- hackernews
---
### Correctifs de sécurité critiques pour Cisco : SD-WAN, IOS XE et IMC

Cisco a déployé des correctifs pour 12 vulnérabilités critiques affectant ses solutions **Catalyst SD-WAN** et **IOS XE**, ainsi que pour deux failles dans l'**Integrated Management Controller (IMC)**. Ces vulnérabilités, identifiées lors d'audits internes et assistées par des modèles d'IA, ne font pas l'objet d'exploitations actives connues à ce jour, à l'exception de CVE-2026-20200 pour laquelle une preuve de concept (PoC) existe.

#### Points clés
*   **Portée :** Les failles touchent les logiciels Cisco Catalyst SD-WAN (toutes configurations) et Cisco IOS XE (modes autonome ou contrôleur).
*   **Gravité :** Plusieurs vulnérabilités présentent un score CVSS critique allant jusqu'à 9.9.
*   **Risque IMC :** La faille CVE-2026-20200 permet à un attaquant distant authentifié de s'élever au niveau root, compromettant potentiellement le BIOS et le SecureBoot, rendant l'attaque persistante et invisible pour les solutions EDR classiques.

#### Vulnérabilités majeures (Sélection)
*   **Catalyst SD-WAN :**
    *   **CVE-2026-20303, 20304, 20310** (CVSS 9.9) : Problèmes de validation d'entrée, contrôle d'accès et résolution de liens.
*   **IOS XE :**
    *   **CVE-2026-20272** (CVSS 9.8) : Injection de commandes/OS.
    *   **CVE-2026-20267** (CVSS 9.0) : Contrôle d'accès inapproprié.
*   **IMC (Cisco Integrated Management Controller) :**
    *   **CVE-2026-20200** (CVSS 8.8) : Exécution de commandes arbitraires permettant une élévation de privilèges root (PoC disponible).

#### Recommandations
*   **Mise à jour immédiate :** Appliquer les correctifs fournis par Cisco pour les versions concernées :
    *   **Catalyst SD-WAN :** Migration vers les versions 20.9.10, 20.12.8.1, 20.15.6, 20.18.4 ou 26.1.2 selon la branche.
    *   **IOS XE :** Passage aux versions 17.9.10, 17.12.8, 17.15.6, 17.18.4/4a ou 26.1.2.
*   **Vigilance :** Consulter les bulletins de sécurité officiels de Cisco pour vérifier les versions spécifiques à votre déploiement.
*   **Priorisation :** En raison de l'existence d'une preuve de concept et de la profondeur de la compromission possible (niveau matériel), le correctif pour l'**IMC** doit être considéré comme une priorité absolue.

---
[Source](https://thehackernews.com/2026/08/cisco-patches-12-sd-wan-and-ios-xe.html){:target="_blank"}
