---
title: 'Microsoft May 2026 Patch Tuesday fixes 120 flaws, no zero-days'
date: 2026-05-12
permalink: /posts/2026/05/12/microsoft-may-2026-patch-tuesday-fixes-120-flaws-no-zero-days/
tags:
- veille-cyber
- bleepingcomp
---
### Correctifs de Sécurité Microsoft : Patch Tuesday de Mai 2026

La mise à jour de sécurité de mai 2026 de Microsoft corrige 120 vulnérabilités, dont 17 sont classées comme « critiques ». Aucune faille « zero-day » n'a été signalée pour cette session.

**Points clés :**
*   **Répartition des failles critiques :** 14 concernent l'exécution de code à distance (RCE), 2 l'élévation de privilèges et 1 la divulgation d'informations.
*   **Menace sur la suite Office :** De multiples vulnérabilités affectant Microsoft Office, Word et Excel permettent l'exécution de code à distance. L'exploitation est possible via l'ouverture de fichiers malveillants, notamment par le volet de prévisualisation.
*   **Périmètre :** Ce décompte exclut les correctifs spécifiques publiés plus tôt dans le mois pour Azure, Copilot, Teams, ainsi que les 131 vulnérabilités traitées par Google pour Chromium/Edge.

**Vulnérabilités critiques notables (sélection) :**
*   **Microsoft Office/Word/Excel :** CVE-2026-42831, CVE-2026-40363, CVE-2026-40358, CVE-2026-40361, CVE-2026-40367, CVE-2026-40366, CVE-2026-40364 (Exécution de code à distance).
*   **SharePoint Server :** CVE-2026-40365 (Exécution de code à distance).
*   **Windows DNS Client :** CVE-2026-41096 (Exécution de code à distance).
*   **Windows Netlogon :** CVE-2026-41089 (Exécution de code à distance).
*   **Windows Native WiFi Miniport Driver :** CVE-2026-32161 (Exécution de code à distance).
*   **Microsoft SSO Plugin (Jira & Confluence) :** CVE-2026-41103 (Élévation de privilèges).
*   **Microsoft Dynamics 365 (On-premises) :** CVE-2026-42898 (Exécution de code à distance).

**Recommandations :**
*   **Mise à jour prioritaire :** Appliquer les correctifs pour Microsoft Office immédiatement, particulièrement pour les utilisateurs recevant fréquemment des pièces jointes.
*   **Vigilance sur la prévisualisation :** Étant donné que le volet de prévisualisation d'Office peut être utilisé comme vecteur d'attaque, la mise à jour des logiciels de bureautique est impérative.
*   **Consultation technique :** Pour une analyse détaillée des systèmes impactés par chaque CVE, il est conseillé de consulter le [rapport complet de Microsoft](https://www.bleepingcomputer.com/microsoft-patch-tuesday-reports/Microsoft-Patch-Tuesday-May-2026.html).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-may-2026-patch-tuesday-fixes-120-flaws-no-zero-days/){:target="_blank"}
