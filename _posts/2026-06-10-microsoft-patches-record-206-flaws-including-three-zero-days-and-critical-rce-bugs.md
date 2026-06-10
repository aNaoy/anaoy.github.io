---
title: 'Microsoft Patches Record 206 Flaws, Including Three Zero-Days and Critical RCE Bugs'
date: 2026-06-10
permalink: /posts/2026/06/10/microsoft-patches-record-206-flaws-including-three-zero-days-and-critical-rce-bugs/
tags:
- veille-cyber
- hackernews
---
### Record de vulnérabilités chez Microsoft : 206 failles corrigées

Microsoft a publié une mise à jour historique corrigeant 206 vulnérabilités au sein de son écosystème logiciel. Cette vague de correctifs, la plus importante à ce jour, inclut 39 failles critiques et 167 vulnérabilités classées comme importantes. Cette tendance à la hausse dans la découverte de failles est largement attribuée à l'utilisation de l'intelligence artificielle pour l'analyse de code.

**Points clés :**
*   **Volume record :** 206 CVE traitées en un seul mois, dépassant le nombre total de vulnérabilités corrigées par Microsoft sur toute l'année 2018.
*   **Zéro-day :** Plusieurs failles étaient déjà divulguées publiquement ou exploitées (notamment *YellowKey*, *bitskrieg*, *GreenPlasma*, *HTTP2/Bomb* et *MiniPlasma*).
*   **Impact :** Les vulnérabilités couvrent l'élévation de privilèges, l'exécution de code à distance (RCE), le contournement de fonctionnalités de sécurité et le déni de service (DoS).

**Vulnérabilités critiques à noter (RCE) :**
*   **CVE-2026-45657 (Score 9.8) :** Faille *Use-after-free* dans le noyau Windows permettant une exécution de code à distance via l'envoi de trafic réseau spécifique.
*   **CVE-2026-47291 (Score 9.8) :** Dépassement d'entier dans `HTTP.sys` permettant l'exécution de code non autorisé.
*   **CVE-2026-44815 (Score 9.8) :** Dépassement de tampon dans le client DHCP, exploitable sans authentification, exposant les services réseau à une compromission totale du système.

**Autres vulnérabilités notables :**
*   **CVE-2026-45585 (Score 6.8) :** Contournement de BitLocker (PoC *YellowKey*).
*   **CVE-2026-49160 (Score 7.5) :** Déni de service dans `HTTP.sys` liée à la technique *HTTP2/Bomb*.
*   **CVE-2026-8863 :** Contournement de la fonctionnalité de sécurité Secure Boot UEFI.

**Recommandations :**
1.  **Application immédiate des correctifs :** Prioriser les systèmes traitant des fonctions réseau critiques (serveurs DHCP, serveurs IIS) ainsi que les systèmes exposés à Internet.
2.  **Configuration spécifique :** Pour contrer l'attaque *HTTP2/Bomb*, activer le paramètre de registre `MaxHeadersCount` afin de limiter le nombre d'en-têtes HTTP/2 et HTTP/3.
3.  **Surveillance accrue :** Compte tenu de la découverte constante de nouvelles failles par des outils d'IA, maintenir une politique de gestion des correctifs rigoureuse et réactive.
4.  **Audit physique :** Renforcer la sécurité physique des terminaux pour limiter les risques liés aux vulnérabilités de contournement de chiffrement (type BitLocker).

---
[Source](https://thehackernews.com/2026/06/microsoft-patches-record-206-flaws.html){:target="_blank"}
