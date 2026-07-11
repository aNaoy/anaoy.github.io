---
title: 'Australia warns of global campaign targeting vulnerable CMS platforms'
date: 2026-07-11
permalink: /posts/2026/07/11/australia-warns-of-global-campaign-targeting-vulnerable-cms-platforms/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne mondiale d'exploitation des systèmes de gestion de contenu (CMS)

Le centre australien de cybersécurité (ACSC) a émis une alerte concernant une campagne mondiale massive visant les plateformes CMS et leurs plugins. Les attaquants scannent activement les sites web pour déployer des « webshells », offrant un accès persistant, la possibilité de voler des identifiants, d'exfiltrer des données ou de servir de point d'entrée pour une compromission plus large du réseau. Cette campagne, potentiellement assistée par l'intelligence artificielle, cible particulièrement les petites et moyennes entreprises.

**Points clés :**
*   **Mode opératoire :** Exploitation automatisée de vulnérabilités connues pour installer des portes dérobées (webshells).
*   **Cibles :** Diverses plateformes, dont WordPress (majoritaire), Craft CMS, MaxSite CMS, MetInfo CMS et Joomla.
*   **Risques :** Interruption de services, vol de données, installation de logiciels malveillants et mouvement latéral au sein du réseau.

**Vulnérabilités exploitées (liste non exhaustive) :**
*   **WordPress (Plugins) :**
    *   Simple File List : CVE-2025-34085, CVE-2020-36847
    *   WavePlayer : CVE-2025-12057
    *   BerqWP : CVE-2025-7443
    *   WPBookit : CVE-2025-7852
    *   Ninja Forms : CVE-2026-0740
    *   ThemeREX Addons : CVE-2026-1969
    *   Breeze Cache : CVE-2026-3844
    *   pay-uz : CVE-2026-31843
    *   ACF Extended : CVE-2025-13486
    *   Sneeit Framework : CVE-2025-6389
    *   WPvivid Backup : CVE-2026-1357
    *   Gravity Forms : CVE-2025-12352
    *   GutenKit/Hunk Companion : CVE-2024-9234
*   **Autres CMS :**
    *   Craft CMS : CVE-2025-32432
    *   MaxSite CMS : CVE-2026-3395
    *   MetInfo CMS : CVE-2026-29014
    *   Joomla JCE : CVE-2026-48907

**Recommandations de sécurité :**
*   **Mise à jour immédiate :** Installer systématiquement les derniers correctifs pour le CMS, les thèmes et l'ensemble des plugins.
*   **Hygiène logicielle :** Supprimer les composants inutilisés et activer les mises à jour automatiques.
*   **Renforcement technique :**
    *   Rendre les répertoires web en « lecture seule » lorsque cela est possible.
    *   Restreindre strictement l'accès aux répertoires sensibles.
    *   Monitorer la création de fichiers suspects et bloquer le lancement inattendu de processus enfants sur le serveur web.

---
[Source](https://www.bleepingcomputer.com/news/security/australia-warns-of-global-campaign-targeting-vulnerable-cms-platforms/){:target="_blank"}
