---
title: 'Microsoft April 2026 Patch Tuesday fixes 167 flaws, 2 zero-days'
date: 2026-04-14
permalink: /posts/2026/04/14/microsoft-april-2026-patch-tuesday-fixes-167-flaws-2-zero-days/
tags:
- veille-cyber
- bleepingcomp
---
### Microsoft Patch Tuesday : 167 vulnérabilités corrigées dont 2 zero-days

La mise à jour de sécurité Microsoft d'avril 2026 apporte des correctifs pour 167 failles, dont 8 classées comme « critiques » (7 exécutions de code à distance et 1 déni de service). Ce bilan exclut les mises à jour pour Edge/Chromium ainsi que les correctifs Azure, Mariner et Bing déployés plus tôt dans le mois.

**Points clés :**
*   **Zero-days :** Deux vulnérabilités zero-day sont traitées : l'une a été divulguée publiquement et l'autre est activement exploitée.
*   **Exploitation active :** Une faille de spoofing dans **Microsoft SharePoint Server** fait l'objet d'attaques actives, permettant à un attaquant non authentifié de consulter ou de modifier des informations sensibles via le réseau.
*   **Élévation de privilèges :** Une vulnérabilité critique dans **Microsoft Defender** permet d'obtenir des privilèges de type SYSTEM.

**Vulnérabilités critiques notables :**
*   **CVE-2026-33115 / CVE-2026-33114 :** Exécution de code à distance dans Microsoft Word.
*   **CVE-2026-32190 :** Exécution de code à distance dans Microsoft Office.
*   **CVE-2026-32157 :** Exécution de code à distance dans le client Bureau à distance (Remote Desktop Client).
*   **CVE-2026-33824 :** Exécution de code à distance dans l'extension IKE de Windows.
*   **CVE-2026-33826 :** Exécution de code à distance dans Active Directory.
*   **CVE-2026-33827 :** Exécution de code à distance dans Windows TCP/IP.
*   **CVE-2026-23666 :** Déni de service dans .NET Framework.

**Recommandations :**
*   **Mises à jour prioritaires :** Appliquer en priorité les correctifs pour Microsoft Office (Word et Excel) afin de contrer les risques d'exécution de code à distance via l'ouverture de documents malveillants ou le volet de prévisualisation.
*   **Mise à jour Defender :** S'assurer que la plateforme antimalware est à jour (version **4.18.26050.3011** ou ultérieure). La mise à jour est généralement automatique, mais peut être forcée via *Sécurité Windows > Protection contre les virus et menaces > Mises à jour de protection*.
*   **Maintenance générale :** Déployer l'ensemble des correctifs de sécurité fournis ce mois-ci pour couvrir les 167 failles identifiées. Le rapport complet est disponible sur le portail MSRC de Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-april-2026-patch-tuesday-fixes-167-flaws-2-zero-days/){:target="_blank"}
