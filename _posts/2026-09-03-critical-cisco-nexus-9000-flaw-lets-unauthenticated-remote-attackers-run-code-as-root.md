---
title: 'Critical Cisco Nexus 9000 Flaw Lets Unauthenticated Remote Attackers Run Code as Root'
date: 2026-09-03
permalink: /posts/2026/09/03/critical-cisco-nexus-9000-flaw-lets-unauthenticated-remote-attackers-run-code-as-root/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques affectant les équipements Cisco

Cisco a publié des correctifs majeurs pour plusieurs de ses gammes d'équipements, notamment pour une faille critique affectant certains commutateurs Nexus 9000 et une série de vulnérabilités impactant le système d'exploitation IOS XR.

**Points clés :**
*   **Nexus 9000 :** Une vulnérabilité permet à un attaquant non authentifié d'exécuter du code à distance avec des privilèges root.
*   **IOS XR :** Une campagne de renforcement a été lancée, regroupant 7 vulnérabilités (dont deux notées 9.8/10), nécessitant des mises à jour logicielles et l'application de correctifs (SMU).
*   **Contexte de menace :** Ces mises à jour surviennent dans un climat de vigilance accrue suite à la découverte d'implants malveillants utilisés par le groupe cybercriminel "Fire Ant" pour infiltrer des routeurs IOS XR.

**Vulnérabilités majeures :**
*   **CVE-2026-20212 (Score CVSS 9.8) :** Faille critique sur les commutateurs Nexus 9000 (modèles spécifiques basés sur "Silicon One"). L'attaquant peut se connecter aux ports TCP 43210 ou 43211 et exécuter du code à distance.
*   **CVE-2026-20274 & CVE-2026-20279 (Score CVSS 9.8) :** Vulnérabilités affectant IOS XR concernant la gestion mémoire, le cycle de vie des ressources et le contrôle d'accès.

**Recommandations :**
*   **Pour les Nexus 9000 :**
    *   Utiliser l'outil [Cisco Software Checker](https://sec.cloudapps.cisco.com/security/center/softwarechecker.x) pour identifier la version de remplacement.
    *   Appliquer, en guise de mesure temporaire, une liste de contrôle d'accès (iACL) bloquant les ports TCP 43210 et 43211.
    *   Si applicable, déployer le "Live Protect shield" (lp00031).
*   **Pour IOS XR :**
    *   Mettre à jour vers les versions recommandées.
    *   Installer les correctifs (SMU) correspondants pour chaque module fonctionnel (BGP, gRPC, IS-IS, OSPF, etc.).
    *   En cas d'utilisation d'une version non répertoriée, contacter le centre d'assistance technique (TAC) de Cisco.

---
[Source](https://thehackernews.com/2026/09/critical-cisco-nexus-9000-flaw-lets.html){:target="_blank"}
