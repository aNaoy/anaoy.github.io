---
title: 'Signal adds encypted local backup support to iOS, desktop apps'
date: 2026-09-30
permalink: /posts/2026/09/30/signal-adds-encypted-local-backup-support-to-ios-desktop-apps/
tags:
- veille-cyber
- bleepingcomp
---
### Sécurisation des sauvegardes Signal : généralisation sur iOS et Desktop

Signal a déployé la version 8.30 de son application, finalisant l'intégration des sauvegardes chiffrées de bout en bout sur l'ensemble de ses plateformes (iOS, Android, Windows, macOS, Linux).

**Points clés :**
*   **Flexibilité des options :** Les utilisateurs peuvent choisir entre des sauvegardes hébergées par Signal (limitées en taille pour les comptes gratuits) ou des sauvegardes locales sur l'appareil (sans restriction de taille).
*   **Interopérabilité :** Un format de sauvegarde unifié permet désormais le transfert direct entre appareils (notamment iPhone vers iPhone via Wi-Fi Aware) et facilite la récupération des historiques lors du jumelage.
*   **Optimisation du stockage :** Les fichiers multimédias sont désormais stockés séparément des archives, réduisant les doublons et permettant aux abonnés payants de libérer de l'espace en ne conservant que des vignettes.
*   **Messages éphémères :** Les messages programmés pour disparaître en moins de 24 heures sont exclus des sauvegardes pour garantir la confidentialité.

**Vulnérabilités et menaces :**
*   **Cible prioritaire :** La clé de récupération, indispensable au déchiffrement des sauvegardes, est devenue une cible active pour les acteurs malveillants. Aucune CVE spécifique n'est associée, car il s'agit d'une menace liée à l'ingénierie sociale ou au vol physique/logique de la clé.

**Recommandations :**
*   **Gestion rigoureuse des clés :** La protection de la clé de récupération est critique. En cas de compromission de cette clé, l'intégralité des sauvegardes chiffrées devient vulnérable.
*   **Sauvegarde redondante :** Pour une résilience optimale, il est conseillé de combiner les options de sauvegarde (locale et hébergée), tout en gardant à l'esprit que la sécurité repose exclusivement sur la gestion secrète de la clé de récupération.
*   **Mise à jour :** S'assurer que tous les clients Signal sont mis à jour vers la version 8.30 pour bénéficier des correctifs de format et des améliorations de transfert.

---
[Source](https://www.bleepingcomputer.com/news/security/signal-adds-encypted-local-backup-support-to-ios-desktop-apps/){:target="_blank"}
