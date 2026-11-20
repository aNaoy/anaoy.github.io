---
title: 'New Unpatched Windows 0-Day FastUnlock Lets Someone Holding a Locked PC Run Programs on It'
date: 2026-11-20
permalink: /posts/2026/11/20/new-unpatched-windows-0-day-fastunlock-lets-someone-holding-a-locked-pc-run-programs-on-it/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité Zero-Day "FastUnlock" sur Windows

Une nouvelle vulnérabilité non corrigée, baptisée **FastUnlock**, permet à une personne disposant d'un accès physique à un ordinateur Windows verrouillé d'exécuter des programmes sans authentification. Bien que l'accès soit limité à un compte utilisateur restreint (ne disposant pas des privilèges administrateur), cette faille compromet la sécurité de l'écran de verrouillage.

**Points clés :**
*   **Méthodologie :** L'attaque exploite l'outil "Narrateur" de Windows via les options de récupération sur l'écran de verrouillage.
*   **Conditions d'exploitation :** Nécessite un accès physique à la machine et l'utilisation d'un compte Microsoft accessible.
*   **Chiffrement :** Le chiffrement BitLocker n'est pas contourné, mais la vulnérabilité fonctionne dès lors que le disque est automatiquement déverrouillé par la puce TPM au démarrage.
*   **État :** Aucune correction n'est disponible à ce jour et aucun cas d'exploitation réelle n'a été signalé.

**Vulnérabilités :**
*   **Identifiant CVE :** Non assigné (Zero-day).

**Recommandations :**
*   **Protection BitLocker :** Configurer un code PIN de démarrage pour BitLocker afin d'empêcher le déverrouillage automatique via le TPM.
*   **Gestion physique :** Sécuriser physiquement les équipements (ordinateurs portables, postes partagés) pour éviter tout accès non autorisé.
*   **Gestion de l'alimentation :** Éteindre ou mettre en veille prolongée les appareils lorsqu'ils ne sont pas sous surveillance directe.
*   **Vigilance :** Ne pas se reposer uniquement sur le verrouillage de session comme mesure de sécurité suffisante pour les données sensibles.

---
[Source](https://thehackernews.com/2026/11/new-unpatched-windows-0-day-fastunlock.html){:target="_blank"}
