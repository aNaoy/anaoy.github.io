---
title: 'Microsoft releases Windows 10 KB5099539 extended security update'
date: 2026-07-14
permalink: /posts/2026/07/14/microsoft-releases-windows-10-kb5099539-extended-security-update/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour de sécurité Windows 10 : KB5099539

Microsoft a publié la mise à jour KB5099539 pour Windows 10, incluant les correctifs du « Patch Tuesday » de juillet 2026. Cette mise à jour corrige un total record de 570 vulnérabilités, dont trois failles « zero-day » (deux étant activement exploitées). Parallèlement, Microsoft a prolongé le programme de mises à jour de sécurité étendues (ESU) pour les particuliers jusqu'au 12 octobre 2027.

**Points clés :**
*   **Versions concernées :** Windows 10 (build 19045.7548) et Windows 10 Enterprise LTSC 2021 (build 19044.7548).
*   **Renforcement de la sécurité réseau :** Durcissement des exigences d'enregistrement pour les transports TDI.
*   **Sécurité RDP :** Ajout du support des empreintes numériques de certificats SHA-2 pour les éditeurs RDP de confiance (le SHA-1 est progressivement abandonné).
*   **Secure Boot :** Amélioration du reporting dynamique dans l'application Sécurité Windows et déploiement de nouveaux certificats.

**Vulnérabilités :**
*   Le correctif englobe 570 vulnérabilités au total, incluant deux failles « zero-day » exploitées et une divulguée publiquement. Bien que l'article ne liste pas les CVE spécifiques, il souligne l'urgence d'appliquer ces correctifs compte tenu de l'exploitation active.

**Recommandations :**
*   **Installation :** Les utilisateurs éligibles doivent effectuer manuellement une recherche via « Windows Update » dans les paramètres du système.
*   **Compatibilité TDI :** Vérifier les journaux d'événements système (ID d'événement 16003) pour identifier les applications héritées qui pourraient cesser de fonctionner suite au durcissement des transports TDI.
*   **Migration RDP :** Les administrateurs informatiques doivent migrer vers l'utilisation d'empreintes SHA-256 (ou algorithmes supérieurs) pour leurs connexions Bureau à distance afin d'éviter toute interruption de service future.
*   **Gestion des fichiers RDP :** Utiliser les politiques de groupe (GPO) pour restreindre l'ouverture des fichiers `.rdp` et limiter les risques de phishing.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-10-kb5099539-extended-security-update/){:target="_blank"}
