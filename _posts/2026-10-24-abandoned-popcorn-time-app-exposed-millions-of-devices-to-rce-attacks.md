---
title: 'Abandoned Popcorn Time app exposed millions of devices to RCE attacks'
date: 2026-10-24
permalink: /posts/2026/10/24/abandoned-popcorn-time-app-exposed-millions-of-devices-to-rce-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans Time4Popcorn : Risque d'exécution de code à distance

L'application abandonnée Time4Popcorn, un fork du client BitTorrent Popcorn Time, présentait une faille majeure exposant des millions d'utilisateurs à une prise de contrôle totale de leur système. Des chercheurs d'Eye Security ont neutralisé cette menace en prenant le contrôle du domaine utilisé par le mécanisme de mise à jour vulnérable.

**Points clés :**
*   **Portée :** Plus de 3 millions d'utilisateurs Windows et 350 000 sous macOS étaient exposés, incluant des réseaux résidentiels, gouvernementaux et militaires.
*   **Méthode de neutralisation :** Les chercheurs ont enregistré le domaine abandonné (*popcorntimeupd.xyz*) pour déployer un correctif à distance désactivant le service de mise à jour sur les machines cibles, sans collecter de données personnelles.
*   **Persistance du risque :** Bien que les systèmes Windows et macOS soient sécurisés, les utilisateurs Android restent vulnérables et l'application utilise une version obsolète de Chrome dépourvue de protections "bac à sable" (sandbox).

**Vulnérabilité identifiée :**
*   **CVE-2026-30612 :** Le système de mise à jour communiquait via HTTP non chiffré et n'effectuait aucune vérification de signature numérique sur les exécutables téléchargés. Cela permettait à un attaquant d'injecter du code malveillant s'exécutant avec les privilèges **SYSTEM** (Windows) ou **root** (macOS).

**Recommandations :**
*   **Suppression immédiate :** La recommandation principale est la désinstallation totale et définitive de l'application Time4Popcorn de tous les appareils.
*   **Attention aux forks :** Éviter d'utiliser des logiciels abandonnés ou issus de sources non officielles, ces derniers manquant de maintenance de sécurité critique.

---
[Source](https://www.bleepingcomputer.com/news/security/abandoned-popcorn-time-app-exposed-millions-of-device-to-rce-attacks/){:target="_blank"}
