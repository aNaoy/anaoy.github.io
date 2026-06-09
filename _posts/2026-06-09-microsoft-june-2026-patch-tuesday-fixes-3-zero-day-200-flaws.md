---
title: 'Microsoft June 2026 Patch Tuesday fixes 3 zero-day, 200 flaws'
date: 2026-06-09
permalink: /posts/2026/06/09/microsoft-june-2026-patch-tuesday-fixes-3-zero-day-200-flaws/
tags:
- veille-cyber
- bleepingcomp
---
### Patch Tuesday de juin 2026 : Correction de 200 vulnérabilités et de 3 failles Zero-Day

La mise à jour de sécurité de juin 2026 pour Microsoft corrige 200 vulnérabilités, dont 33 classées « Critiques ». Parmi ces correctifs, trois concernent des vulnérabilités Zero-Day divulguées publiquement, bien qu'aucune exploitation active n'ait été signalée à ce jour.

#### Points clés
*   **Répartition des vulnérabilités critiques :** 28 failles d'exécution de code à distance (RCE), 4 d'élévation de privilèges et 1 de divulgation d'informations.
*   **Zero-Days corrigés :**
    *   **Windows CTFMON :** Une faille permettant d'obtenir des privilèges SYSTEM via une résolution de liens incorrecte.
    *   **HTTP/2 Bomb (DoS) :** Une attaque exploitant la gestion de la compression des en-têtes HTTP/2 pour saturer la mémoire des serveurs.
    *   **BitLocker (YellowKey) :** Un contournement de sécurité via une attaque physique (USB/EFI) permettant d'accéder aux lecteurs chiffrés sur des systèmes utilisant une protection TPM uniquement.

#### Recommandations
*   **Appliquer les correctifs :** Déployer sans délai les mises à jour de sécurité de juin 2026.
*   **Atténuation HTTP/2 :** Microsoft a introduit une nouvelle clé de registre `MaxHeadersCount` pour limiter le nombre d'en-têtes HTTP/2 et HTTP/3 (voir KB5102602).
*   **Renforcement BitLocker :** Pour les systèmes utilisant uniquement le TPM, il est fortement recommandé d'activer l'authentification combinée **TPM + PIN** pour contrer les attaques de type « YellowKey ».

#### Vulnérabilités Zero-Day identifiées (CVE non spécifiés dans l'article pour ces points précis)
L'article détaille également un large éventail de vulnérabilités via son bulletin, notamment :
*   **RCE (Critiques) :** Active Directory (CVE-2026-45648), Azure Kubernetes Service (CVE-2026-32193), Microsoft Office (ex: CVE-2026-45463, CVE-2026-45458), Windows Hyper-V (CVE-2026-45641).
*   **Élévation de privilèges (Critique) :** Azure Network Adapter (CVE-2026-45476) et Windows Device Health Attestation (CVE-2026-33828).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-june-2026-patch-tuesday-fixes-3-zero-day-200-flaws/){:target="_blank"}
