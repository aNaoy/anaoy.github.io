---
title: 'Adobe Patches 7 CVSS 10.0 Flaws in ColdFusion and Campaign Classic'
date: 2026-07-01
permalink: /posts/2026/07/01/adobe-patches-7-cvss-100-flaws-in-coldfusion-and-campaign-classic/
tags:
- veille-cyber
- hackernews
---
### Alertes de sécurité critiques : Adobe corrige sept vulnérabilités de score 10.0

Adobe a publié des correctifs urgents pour corriger plusieurs failles de sécurité critiques affectant **Adobe ColdFusion** et **Adobe Campaign Classic**. Ces vulnérabilités permettent, dans les cas les plus graves, une exécution arbitraire de code.

**Points clés :**
*   **Gravité :** Sept vulnérabilités présentent un score CVSS maximal de 10.0.
*   **Changement de politique :** En raison de l'accélération de la détection des failles par l'IA, Adobe passera à un rythme de publication bimensuel à compter du 14 juillet 2026.
*   **Exploitation :** Aucune preuve d'exploitation active n'a été constatée à ce jour.

**Vulnérabilités majeures (Score CVSS 10.0) :**
*   **ColdFusion (CVE-2026-48276, CVE-2026-48283) :** Téléversement non restreint de fichiers dangereux.
*   **ColdFusion (CVE-2026-48277, CVE-2026-48281, CVE-2026-48316) :** Défaut de validation des entrées.
*   **ColdFusion (CVE-2026-48282) :** Traversée de répertoire.
*   **Campaign Classic (CVE-2026-48286) :** Autorisation incorrecte (affecte uniquement les instances sur site).

*Autres vulnérabilités notables :* CVE-2026-48313 (traversée de répertoire, score 9.3) et CVE-2026-48315 (validation des entrées, score 9.3).

**Recommandations :**
*   **ColdFusion :** Mettre à jour vers la version **2023 Update 21** ou **2025 Update 10**.
*   **Campaign Classic :** Mettre à jour vers la version **ACC v7: 7.4.3 build 9397** pour les déploiements sur site (les instances hébergées par Adobe sont déjà corrigées).

---
[Source](https://thehackernews.com/2026/07/adobe-patches-7-cvss-100-flaws-in.html){:target="_blank"}
