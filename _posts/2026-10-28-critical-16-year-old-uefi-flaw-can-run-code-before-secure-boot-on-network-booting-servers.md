---
title: 'Critical 16-Year-Old UEFI Flaw Can Run Code Before Secure Boot on Network-Booting Servers'
date: 2026-10-28
permalink: /posts/2026/10/28/critical-16-year-old-uefi-flaw-can-run-code-before-secure-boot-on-network-booting-servers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans l'UEFI : Risque d'exécution de code via PXE

Une faille critique, présente depuis 16 ans dans le code source EDK II (utilisé par la majorité des constructeurs de firmware UEFI), expose les serveurs et équipements réseau utilisant le démarrage PXE. Cette vulnérabilité permet à un attaquant distant d'exécuter du code arbitraire avant même le chargement du démarrage sécurisé (Secure Boot).

**Points clés :**
*   **Nature de la faille :** Un dépassement de tampon (*buffer overflow*) dans le code de gestion réseau (PXE) de l'UEFI.
*   **Vecteur d'attaque :** L'attaquant doit envoyer un message réseau malveillant vers la machine ciblée précisément au moment où celle-ci effectue un démarrage via le réseau.
*   **Impact :** Crash du système, contournement des mesures de sécurité au démarrage, ou persistance par installation de code malveillant.
*   **Disponibilité :** Aucune exploitation active n'a été signalée à ce jour, mais la divulgation prématurée du correctif rend la création d'exploits possible pour des attaquants compétents.

**Vulnérabilité identifiée :**
*   **CVE-2026-97631** (Score CVSS : 9.5/10).

**Recommandations :**
*   **Désactivation :** Pour les environnements où le démarrage réseau n'est pas requis, désactiver la fonctionnalité PXE dans le BIOS/UEFI constitue la mesure de protection la plus efficace.
*   **Surveillance :** Surveiller les logs réseau et le trafic lors des phases de démarrage pour détecter toute anomalie ou tentative de connexion inhabituelle.
*   **Mise à jour :** Bien qu'un correctif soit intégré dans le code source EDK II, il est nécessaire d'attendre que les fabricants de serveurs et de matériel publient des mises à jour spécifiques du micrologiciel (BIOS/UEFI) intégrant cette correction. Il est conseillé de surveiller les avis de sécurité des constructeurs.

---
[Source](https://thehackernews.com/2026/10/critical-16-year-old-uefi-flaw-can-run.html){:target="_blank"}
