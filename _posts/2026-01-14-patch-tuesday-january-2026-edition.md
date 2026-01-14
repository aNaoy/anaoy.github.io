---
title: 'Patch Tuesday, January 2026 Edition'
date: 2026-01-14
permalink: /posts/2026/01/14/patch-tuesday-january-2026-edition/
tags:
- veille-cyber
- krebs
---
**Mises à jour de sécurité Janvier 2026 : Défauts et Corrections**

Microsoft a publié des correctifs pour 113 vulnérabilités, dont 8 jugées critiques. Une faille, **CVE-2026-20805**, affectant le Desktop Window Manager, est déjà exploitée par des attaquants. Bien que classée comme "Importante" avec un score CVSS de 5.5, cette vulnérabilité peut être utilisée pour contourner des mesures de sécurité comme l'ASLR, facilitant ainsi des attaques complexes.

D'autres failles critiques incluent deux vulnérabilités d'exécution de code à distance dans Microsoft Office (**CVE-2026-20952**, **CVE-2026-20953**), activables via le volet d'aperçu. Microsoft a également retiré deux pilotes de modem vieillissants, dont un précédemment vulnérable (**CVE-2023-31096**), en raison de préoccupations similaires concernant des failles d'élévation de privilèges dans du matériel ancien.

Une vulnérabilité critique de contournement de fonctionnalités de sécurité (**CVE-2026-21265**) touche le démarrage sécurisé de Windows. Ce système repose sur des certificats arrivant à expiration, nécessitant des mises à jour pour maintenir la protection contre les rootkits.

Des mises à jour de sécurité ont également été publiées pour Mozilla Firefox (résolvant 34 vulnérabilités, dont 2 potentiellement exploitées : **CVE-2026-0891**, **CVE-2026-0892**) et Google Chrome (incluant la résolution d'une vulnérabilité dans Chrome WebView : **CVE-2026-0628**). Des mises à jour pour Google Chrome et Microsoft Edge sont attendues.

**Points Clés :**

*   Plus de 113 vulnérabilités corrigées par Microsoft.
*   Une vulnérabilité critique (CVE-2026-20805) déjà exploitée activement.
*   Deux failles critiques dans Microsoft Office (CVE-2026-20952, CVE-2026-20953).
*   Retrait de pilotes de modem obsolètes suite à des vulnérabilités (CVE-2023-31096).
*   Vulnérabilité critique du démarrage sécurisé (CVE-2026-21265) liée à l'expiration de certificats.
*   Mises à jour pour Firefox et Chrome.

**Vulnérabilités :**

*   **CVE-2026-20805** (Desktop Window Manager, exploitation active)
*   **CVE-2026-20952** (Microsoft Office, exécution de code à distance)
*   **CVE-2026-20953** (Microsoft Office, exécution de code à distance)
*   **CVE-2023-31096** (Pilote modem Agere, élévation de privilèges)
*   **CVE-2026-21265** (Démarrage sécurisé, contournement de fonctionnalité de sécurité)
*   **CVE-2026-0891** (Firefox, potentiellement exploité)
*   **CVE-2026-0892** (Firefox, potentiellement exploité)
*   **CVE-2026-0628** (Chrome WebView)

**Recommandations :**

*   Appliquer les correctifs de sécurité Microsoft dès que possible.
*   Pour CVE-2026-20805, le patch rapide est la seule mitigation efficace.
*   Être vigilant quant à l'exploitation potentielle de CVE-2023-31096 et des pilotes de modem similaires.
*   Préparer attentivement les mises à jour du chargeur de démarrage et du BIOS pour mitiger CVE-2026-21265 afin d'éviter des problèmes de démarrage.
*   Mettre à jour Mozilla Firefox et les navigateurs tels que Google Chrome et Microsoft Edge.
*   Suivre les recommandations du SANS Internet Storm Center et d'askwoody.com pour les éventuels problèmes d'installation de correctifs.

---
[Source](https://krebsonsecurity.com/2026/01/patch-tuesday-january-2026-edition/){:target="_blank"}
