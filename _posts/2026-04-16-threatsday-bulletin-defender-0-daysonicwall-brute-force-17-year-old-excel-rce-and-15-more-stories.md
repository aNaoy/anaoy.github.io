---
title: 'ThreatsDay Bulletin: Defender 0-Day, SonicWall Brute-Force, 17-Year-Old Excel RCE and 15 More Stories'
date: 2026-04-16
permalink: /posts/2026/04/16/threatsday-bulletin-defender-0-daysonicwall-brute-force-17-year-old-excel-rce-and-15-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces et vulnérabilités : Avril 2026

Le paysage actuel de la cybersécurité est marqué par une recrudescence d'attaques sophistiquées ciblant la chaîne d'approvisionnement, des vulnérabilités exploitées dans des logiciels hérités et des campagnes de fraude industrielle.

#### Points clés
*   **Chaîne d'approvisionnement :** Un piratage de la suite de plugins "Essential Plugin" a permis d'injecter des backdoors sur plus de 180 000 sites WordPress.
*   **Fraude et Scams :** Une application contrefaite "Ledger Live" sur l'App Store d'Apple a dérobé 9,5 millions de dollars. Parallèlement, le réseau "Triad Nexus" continue ses activités de blanchiment et d'usurpation de marque malgré les sanctions internationales.
*   **Espionnage :** Le groupe APT41 déploie des backdoors persistantes sur des infrastructures cloud (AWS, Azure, Google Cloud, Alibaba) en utilisant le port SMTP 25 pour le C2.
*   **Évolution des défenses :** Raspberry Pi OS renforce sa sécurité par défaut en exigeant un mot de passe pour les commandes `sudo`. Google durcit sa politique contre le "back button hijacking".

#### Vulnérabilités majeures
*   **Microsoft Defender (RedSun) :** Nouvelle vulnérabilité d'escalade de privilèges (non patchée au moment de la publication) permettant de passer d'un utilisateur non privilégié à SYSTEM.
*   **Microsoft Office Excel (CVE-2009-0238) :** Vulnérabilité critique (Score CVSS 8.8) d'exécution de code à distance (RCE) vieille de 17 ans, désormais activement exploitée et ajoutée au catalogue KEV de la CISA.
*   **Windows RDP (CVE-2026-26151) :** Abus des fichiers de configuration RDP pour le phishing. Microsoft a intégré des avertissements de sécurité et désactivé certaines redirections par défaut.
*   **Microsoft SharePoint (CVE-2026-33825) :** Patché lors du *Patch Tuesday* d'avril 2026 (lié à l'exploit "BlueHammer").

#### Recommandations
*   **Gestion des accès :** Appliquer le principe du moindre privilège, particulièrement sur les environnements Linux (désactivation du `sudo` sans mot de passe).
*   **Hygiène logicielle :** Mettre à jour immédiatement tous les composants Office et examiner les plugins tiers sur les sites web (suppression des extensions obsolètes ou suspectes).
*   **Vigilance périphérique :** Surveiller étroitement les tentatives de brute-force sur les boîtiers de périmètre (SonicWall, FortiGate), avec une attention particulière sur les connexions provenant de zones géographiques inhabituelles.
*   **Prudence applicative :** Ne pas se fier aveuglément aux applications présentes sur les stores officiels ; vérifier systématiquement l'éditeur avant installation.
*   **Sécurité RDP :** Désactiver les redirections de ressources locales dans les fichiers RDP pour contrer les vecteurs de phishing actuels.

---
[Source](https://thehackernews.com/2026/04/threatsday-bulletin-17-year-old-excel.html){:target="_blank"}
