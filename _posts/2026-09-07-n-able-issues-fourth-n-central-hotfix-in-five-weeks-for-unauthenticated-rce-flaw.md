---
title: 'N-able Issues Fourth N-central Hotfix in Five Weeks for Unauthenticated RCE Flaw'
date: 2026-09-07
permalink: /posts/2026/09/07/n-able-issues-fourth-n-central-hotfix-in-five-weeks-for-unauthenticated-rce-flaw/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique RCE dans N-able N-central : Hotfix d'urgence

N-able a publié son quatrième correctif (Hotfix 4) en cinq semaines pour la plateforme de gestion et de surveillance à distance (RMM) N-central, afin de corriger une vulnérabilité critique permettant l'exécution de code à distance (RCE) sans authentification.

**Points clés :**
*   **Gravité maximale :** La vulnérabilité est classée avec un score CVSS 4.0 de 10.0.
*   **Exploitation :** Il existe une divergence dans les communications de N-able ; certaines documentations indiquent une exploitation active ("in the wild"), tandis que d'autres mentionnent l'absence de confirmation d'exploitation.
*   **Historique :** Il s'agit du quatrième correctif depuis début août, illustrant une période de fragilité sécuritaire marquée pour cette plateforme.

**Vulnérabilité identifiée :**
*   **CVE-2026-86218 :** Injection de code statique (CWE-96) permettant une RCE pré-authentification.

**Recommandations :**
*   **Mise à jour immédiate :** Tous les clients utilisant une version inférieure à la **2026.3.1.14** doivent appliquer ce correctif sans délai.
*   **Sécurisation périmétrique :** Dans l'attente de l'application du correctif, il est fortement conseillé de restreindre l'accès à la console N-central via une liste d'adresses IP autorisées (allowlisting) ou un VPN.
*   **Déconnexion préventive :** Si le serveur est exposé directement sur Internet, envisagez de le mettre hors ligne jusqu'à ce que la mise à jour soit effectuée.
*   **Audit :** Vérifiez régulièrement les comptes utilisateurs dans N-central afin de détecter toute création d'utilisateur non autorisée ou suspecte.

---
[Source](https://thehackernews.com/2026/09/n-able-issues-fourth-n-central-hotfix.html){:target="_blank"}
