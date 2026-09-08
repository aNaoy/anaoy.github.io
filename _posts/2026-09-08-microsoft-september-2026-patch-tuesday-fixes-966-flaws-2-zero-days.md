---
title: 'Microsoft September 2026 Patch Tuesday fixes 966 flaws, 2 zero-days'
date: 2026-09-08
permalink: /posts/2026/09/08/microsoft-september-2026-patch-tuesday-fixes-966-flaws-2-zero-days/
tags:
- veille-cyber
- bleepingcomp
---
### Patch Tuesday Septembre 2026 : 966 failles corrigées par Microsoft

Microsoft a publié une mise à jour corrective massive traitant 966 vulnérabilités, dont 105 sont classées comme « critiques ». Cette vague de correctifs inclut la résolution de deux failles « zero-day » activement exploitées.

#### Points clés
*   **Volume :** 966 vulnérabilités corrigées lors de ce Patch Tuesday (hors 204 correctifs diffusés plus tôt dans le mois).
*   **Répartition des failles critiques :**
    *   81 vulnérabilités d'exécution de code à distance (RCE).
    *   20 vulnérabilités d'élévation de privilèges.
    *   2 divulgations d'informations.
    *   1 contournement de fonctionnalité de sécurité.

#### Vulnérabilités Zero-Day (Exploitées activement)
Deux failles de type élévation de privilèges (EoP) dans Windows ont été activement exploitées pour obtenir des privilèges `SYSTEM` :
1.  **Windows Update Stack :** Vulnérabilité due à un « link following » (résolution de lien inappropriée avant accès au fichier).
2.  **Windows ALPC (Advanced Local Procedure Call) :** Dépassement de tampon basé sur le tas (heap-based buffer overflow).

#### Recommandations
*   **Application immédiate :** Étant donné l'exploitation active des vulnérabilités zero-day, il est impératif de déployer les mises à jour de sécurité sur tous les systèmes Windows affectés.
*   **Priorisation :** Les correctifs traitant les 105 failles critiques, en particulier celles concernant l'exécution de code à distance, doivent être déployés en priorité.
*   **Consultation :** Pour obtenir la liste exhaustive des systèmes affectés par chaque CVE, référez-vous au [rapport complet de Microsoft](https://www.bleepingcomputer.com/microsoft-patch-tuesday-reports/Microsoft-Patch-Tuesday-September-2026.html).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-september-2026-patch-tuesday-fixes-966-flaws-2-zero-days/){:target="_blank"}
