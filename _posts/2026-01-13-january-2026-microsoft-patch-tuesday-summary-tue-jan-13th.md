---
title: 'January 2026 Microsoft Patch Tuesday Summary, (Tue, Jan 13th)'
date: 2026-01-13
permalink: /posts/2026/01/13/january-2026-microsoft-patch-tuesday-summary-tue-jan-13th/
tags:
- veille-cyber
- sans-isc
---
### Point sur les correctifs de sécurité Microsoft de Janvier 2026

Microsoft a publié des correctifs pour 113 vulnérabilités, dont 8 critiques. Une vulnérabilité affectant le navigateur Edge a été corrigée en amont par Chromium. Parmi les vulnérabilités critiques, cinq touchent des composants de Microsoft Office. Une vulnérabilité signalée comme déjà exploitée concerne le Desktop Windows Manager.

**Points clés et Vulnérabilités notables :**

*   **CVE-2026-20854 :** Vulnérabilité d'exécution de code à distance dans LSASS. Nécessite une authentification préalable mais pas de privilèges élevés. Moins susceptible d'être exploitée selon Microsoft.
*   **CVE-2026-20805 :** Vulnérabilité de divulgation d'informations dans le Desktop Windows Manager, déjà exploitée. Permet d'identifier l'adresse de section à partir d'un port ALPC distant.
*   **CVE-2026-21265 :** Le démarrage sécurisé pourrait ne pas reconnaître un certificat expiré. Divulguée précédemment, non exploitée à ce jour.

**Autres vulnérabilités importantes notables :**

*   Azure Connected Machine Agent : Élévation de privilèges (CVE-2026-21224).
*   Bibliothèque cliente partagée Azure Core pour Python : Exécution de code à distance (CVE-2026-21226).
*   Microsoft Office : Plusieurs vulnérabilités critiques et importantes d'exécution de code à distance et d'élévation de privilèges dans Excel (ex: CVE-2026-20955, CVE-2026-20957), Office (ex: CVE-2026-20953, CVE-2026-20952) et Word (ex: CVE-2026-20944).
*   Microsoft SharePoint : Vulnérabilités d'exécution de code à distance et de divulgation d'informations (ex: CVE-2026-20963, CVE-2026-20958).
*   Divers composants Windows : De nombreuses vulnérabilités d'élévation de privilèges et de divulgation d'informations affectant des composants tels que le noyau, LSASS, le gestionnaire de fenêtres, et divers pilotes.

**Recommandations :**

*   Appliquer les correctifs de sécurité fournis par Microsoft dès que possible pour atténuer ces risques.

---
[Source](https://isc.sans.edu/diary/rss/32624){:target="_blank"}
