---
title: 'Microsoft June 2026 Patch Tuesday, (Tue, Jun 9th)'
date: 2026-06-09
permalink: /posts/2026/06/09/microsoft-june-2026-patch-tuesday-tue-jun-9th/
tags:
- veille-cyber
- sans-isc
---
### Analyse du Patch Tuesday de Microsoft - Juin 2026

La mise à jour de juin 2026 est particulièrement dense, avec **204 vulnérabilités corrigées**, dont 38 classées comme critiques. Cette volumétrie importante, notamment concernant les 360 vulnérabilités intégrées dans Chromium pour Edge, illustre l'usage croissant des outils d'IA dans la découverte de failles.

#### Points clés
*   **Solutions Cloud :** Six vulnérabilités affectant les services cloud de Microsoft ont été corrigées sans nécessiter d'intervention client.
*   **Bypass de sécurité :** Trois failles liées au contournement de la sécurité BitLocker ont été résolues.
*   **Applications Office :** Plusieurs vulnérabilités critiques touchent la suite Microsoft Office (Outlook, Word, Excel).

#### Vulnérabilités notables
*   **CVE-2026-49160 (HTTP/2 & HTTP/3) :** Divulgation publique antérieure. La vulnérabilité permet une attaque de type "compression bomb" via l'algorithme HPACK, entraînant une saturation des ressources.
*   **CVE-2026-47291 (http.sys) :** Critique, permettant l'exécution de code à distance (RCE) via une requête surdimensionnée provoquant un dépassement d'entier.
*   **CVE-2026-45648 (Active Directory) :** Dépassement de tampon basé sur la pile. Bien que critique, son exploitation est jugée "peu probable" car elle nécessite une authentification préalable.

#### Recommandations
*   **Mises à jour :** Appliquer les correctifs de sécurité Microsoft dès que possible, en priorité sur les systèmes exposés (serveurs web, serveurs Active Directory).
*   **Atténuation (CVE-2026-49160) :** Configurer le paramètre de registre `MaxHeadersCount` pour limiter l'allocation des ressources.
*   **Atténuation (CVE-2026-47291) :** Restreindre la valeur `MaxRequestBytes` au niveau du serveur web pour prévenir l'exploitation en attendant le déploiement du patch.

---
[Source](https://isc.sans.edu/diary/rss/33064){:target="_blank"}
