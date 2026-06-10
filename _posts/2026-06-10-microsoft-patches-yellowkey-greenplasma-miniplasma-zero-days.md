---
title: 'Microsoft patches YellowKey, GreenPlasma, MiniPlasma zero-days'
date: 2026-06-10
permalink: /posts/2026/06/10/microsoft-patches-yellowkey-greenplasma-miniplasma-zero-days/
tags:
- veille-cyber
- bleepingcomp
---
### Correctifs Microsoft : Neutralisation des vulnérabilités Zero-Day "Plasma" et "YellowKey"

Microsoft a profité de son cycle de mises à jour de juin 2026 pour corriger trois vulnérabilités zero-day critiques, initialement révélées par le chercheur "Nightmare Eclipse" en signe de protestation contre la gestion des divulgations par Microsoft.

#### Points clés
*   **Origine des failles :** Découvertes dans le cadre du Collaborative Translation Framework, du Cloud Files Mini Filter Driver et de l'environnement de récupération Windows (WinRE).
*   **Contexte :** Le chercheur a rendu publics plusieurs exploits (PoC) ces derniers mois, forçant Microsoft à réagir face à des vulnérabilités exploitées activement.
*   **Tensions :** Microsoft a initialement menacé de poursuites judiciaires avant de tempérer sa position face aux critiques de la communauté cyber.

#### Vulnérabilités corrigées
*   **GreenPlasma (CVE-2026-45586) :** Élévation de privilèges locale permettant d'obtenir des droits SYSTEM.
*   **MiniPlasma (CVE-2020-17103) :** Élévation de privilèges locale permettant d'obtenir des droits SYSTEM.
*   **YellowKey (CVE-2026-45585) :** Contournement de la protection BitLocker via une porte dérobée dans l'environnement de récupération (WinRE), nécessitant un accès physique.

#### Recommandations
*   **Mise à jour immédiate :** Appliquer les correctifs du Patch Tuesday de juin 2026 sur tous les systèmes Windows, incluant les serveurs.
*   **Surveillance :** Être particulièrement vigilant face aux nouvelles vulnérabilités signalées par "Nightmare Eclipse" (telles que *RoguePlanet*), dont les preuves de concept sont publiées rapidement après les mises à jour, rendant les systèmes non mis à jour extrêmement vulnérables.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-patches-yellowkey-greenplasma-miniplasma-zero-days/){:target="_blank"}
