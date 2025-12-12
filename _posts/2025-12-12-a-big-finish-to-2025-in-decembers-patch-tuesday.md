---
title: 'A big finish to 2025 in December’s Patch Tuesday'
date: 2025-12-12
permalink: /posts/2025/12/12/a-big-finish-to-2025-in-decembers-patch-tuesday/
tags:
- veille-cyber
- sophos
---
Décembre 2025 : Lancement de mises à jour de sécurité critiques et généralisées

En décembre 2025, Microsoft a publié 56 correctifs concernant 10 familles de produits. Deux de ces correctifs sont classés comme critiques, affectant la famille de produits Office-365. Huit vulnérabilités ont un score CVSS de base de 8.0 ou plus, et parmi elles, une fait l'objet d'exploitations actives tandis que deux autres sont publiquement divulguées. Six CVEs supplémentaires sont jugées plus susceptibles d'être exploitées dans les 30 jours suivant leur publication.

Les vulnérabilités les plus fréquentes concernent les élévations de privilèges (28 CVEs) et l'exécution à distance de code (19 CVEs).

**Vulnérabilités notables et recommandations :**

*   **Exécution à distance de code dans Office et Word :**
    *   CVE-2025-62554, CVE-2025-62555, CVE-2025-62557, CVE-2025-62558, CVE-2025-62559, CVE-2025-62560, CVE-2025-62561.
    *   Ces vulnérabilités affectent plusieurs versions de Microsoft 365 et Office, y compris les versions Mac pour lesquelles les correctifs ne sont pas encore disponibles. Les correctifs CVE-2025-62554 et CVE-2025-62557 sont particulièrement critiques car ils exploitent le volet de prévisualisation.
    *   **Recommandation :** Appliquer les correctifs pour Office et Word dès que possible, et surveiller les mises à jour pour les versions Mac.

*   **Exécution à distance de code dans PowerShell :**
    *   CVE-2025-54100.
    *   Cette vulnérabilité concerne une mauvaise gestion des éléments spéciaux dans une commande. Microsoft recommande l'utilisation du commutateur `-UseBasicParsing` avec la commande `Invoke-WebRequest` après installation du correctif pour maintenir un comportement correct.
    *   **Recommandation :** Installer le correctif et utiliser le commutateur recommandé pour `Invoke-WebRequest`.

*   **Élévation de privilèges et usurpation d'identité dans Exchange Server :**
    *   CVE-2025-64666 (Élévation de privilèges), CVE-2025-64667 (Usurpation d'identité).
    *   Ces deux vulnérabilités affectent les versions 2016 et 2019 d'Exchange Server qui sont hors support, sauf si un contrat de mise à jour de sécurité étendue (ESU) est en place. L'élévation de privilèges nécessite une préparation préalable de l'environnement cible, tandis que le bogue d'usurpation affecte l'affichage des adresses d'expéditeur.
    *   **Recommandation :** Appliquer les correctifs aux versions d'Exchange Server concernées et couvertes par un support.

*   **Exécution à distance de code dans GitHub Copilot pour Jetbrains :**
    *   CVE-2025-6471.
    *   Cette vulnérabilité publiquement divulguée permet à un attaquant d'exécuter des commandes supplémentaires en les ajoutant à celles autorisées dans les paramètres d'approbation automatique du terminal de l'utilisateur.
    *   **Recommandation :** Mettre à jour GitHub Copilot pour Jetbrains.

**Autres informations clés :**

*   **Nombre total de CVEs :** 56
*   **Sévérité critique :** 2
*   **Sévérité importante :** 54
*   **Vulnérabilités exploitées activement :** 1
*   **Vulnérabilités publiquement divulguées :** 2
*   **Vulnérabilités plus susceptibles d'être exploitées dans les 30 jours :** 6
*   **Produits les plus touchés :** Windows (38 CVEs), 365 (13 CVEs), Office (13 CVEs).

De plus, des correctifs ont été publiés pour 14 vulnérabilités dans Microsoft Edge (principalement issues de Chromium), 12 pour ColdFusion et 4 pour Adobe Reader. 84 CVEs affectant CBL Mariner et/ou Azure Linux ont également été corrigés, dont la majorité fait l'objet d'exploitations actives.

Il est conseillé aux administrateurs de télécharger et d'appliquer ces correctifs dès que possible pour atténuer les risques de sécurité. L'année 2025 s'achève avec un nombre élevé de correctifs, soulignant l'importance d'une gestion proactive des mises à jour.

---
[Source](https://news.sophos.com/en-us/2025/12/11/a-big-finish-to-2025-in-decembers-patch-tuesday/){:target="_blank"}
