---
title: 'Microsoft Patch Tuesday, March 2026 Edition'
date: 2026-03-11
permalink: /posts/2026/03/11/microsoft-patch-tuesday-march-2026-edition/
tags:
- veille-cyber
- krebs
---
### Analyse du Patch Tuesday de mars 2026 : 77 vulnérabilités corrigées

La mise à jour mensuelle de Microsoft corrige 77 vulnérabilités. Bien qu’aucune faille « zero-day » ne soit signalée ce mois-ci, l’accent est mis sur une forte prévalence de bugs d’élévation de privilèges et de failles d’exécution de code à distance (RCE) critiques dans Microsoft Office.

#### Points clés
* **Dominance des privilèges :** 55 % des vulnérabilités corrigées concernent l'élévation de privilèges.
* **Innovation IA :** La faille CVE-2026-21536 marque une étape historique : il s'agit de l'une des premières vulnérabilités critiques (score 9.8) identifiée par un agent de test d'intrusion autonome (XBOW), sans accès au code source.
* **Écosystème étendu :** Outre Microsoft, Adobe a corrigé 80 vulnérabilités dans ses produits et Mozilla a mis à jour Firefox pour corriger trois failles de haute sévérité.

#### Vulnérabilités notables
* **Élévation de privilèges (SQL Server) :** **CVE-2026-21262** (Score 8.8) – Permet à un attaquant autorisé d'obtenir des droits *sysadmin* sur le réseau.
* **Exécution de code à distance (Office) :** **CVE-2026-26113** et **CVE-2026-26110** – Exploitables simplement en visualisant un message piégé dans le volet de prévisualisation.
* **Élévation de privilèges (Composants Windows) :** Une série de failles notées "exploitation probable" (score 7.8) touchant divers composants critiques :
    * **CVE-2026-24291** (Infrastructure d'accessibilité)
    * **CVE-2026-24294** (SMB)
    * **CVE-2026-24289** (Corruption mémoire)
    * **CVE-2026-25187** (Winlogon)
* **Déni de service (.NET) :** **CVE-2026-26127** – Déclenche un plantage de l'application.

#### Recommandations
1. **Priorisation immédiate :** Appliquer en priorité les correctifs pour **CVE-2026-21262** (SQL Server) et les failles RCE dans **Microsoft Office** (**CVE-2026-26113/26110**), car celles-ci présentent des risques élevés d'exploitation active.
2. **Surveillance des composants système :** Porter une attention particulière aux vulnérabilités identifiées comme "exploitation plus probable" affectant le noyau, SMB et Winlogon.
3. **Mise à jour multi-logiciels :** Ne pas se limiter à l'écosystème Windows ; procéder également aux mises à jour des produits **Adobe** et du navigateur **Firefox** pour réduire la surface d'attaque globale.
4. **Veille :** Consulter régulièrement des sources comme le *SANS Internet Storm Center* pour suivre les éventuels problèmes liés à l'application de ces correctifs.

---
[Source](https://krebsonsecurity.com/2026/03/microsoft-patch-tuesday-march-2026-edition/){:target="_blank"}
