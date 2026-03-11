---
title: 'Microsoft Patches 84 Flaws in March Patch Tuesday, Including Two Public Zero-Days'
date: 2026-03-11
permalink: /posts/2026/03/11/microsoft-patches-84-flaws-in-march-patch-tuesday-including-two-public-zero-days/
tags:
- veille-cyber
- hackernews
---
### Mise à jour de sécurité Microsoft de mars 2026 : 84 vulnérabilités corrigées

Microsoft a publié son correctif mensuel traitant 84 vulnérabilités, dont huit sont classées comme critiques. La majorité des failles corrigées concernent l'élévation de privilèges (46) et l'exécution de code à distance (18).

**Points clés :**
*   **Zero-days :** Deux vulnérabilités connues publiquement ont été corrigées.
*   **Priorité aux privilèges :** Plus de la moitié des failles traitées permettent une élévation de privilèges, souvent utilisées par des attaquants pour se déplacer latéralement après une compromission initiale.
*   **Modernisation :** Microsoft généralise les "hotpatchs" via Windows Autopatch pour appliquer les correctifs de sécurité sans nécessiter de redémarrage immédiat.

**Vulnérabilités notables :**
*   **CVE-2026-21262 (Score 8.8) :** Élévation de privilèges dans SQL Server (Zero-day).
*   **CVE-2026-26127 (Score 7.5) :** Déni de service dans .NET (Zero-day).
*   **CVE-2026-21536 (Score 9.8) :** Exécution de code à distance dans le *Microsoft Devices Pricing Program* (corrigé, aucune action utilisateur requise).
*   **CVE-2026-25187 (Score 7.8) :** Élévation de privilèges via *Winlogon*, permettant à un utilisateur local d'obtenir des droits SYSTEM.
*   **CVE-2026-26118 (Score 8.8) :** Falsification de requête côté serveur (SSRF) dans *Azure Model Context Protocol*, permettant de détourner des jetons d'identité.
*   **CVE-2026-26144 (Score 7.5) :** Divulgation d'informations dans Excel, exploitable via une attaque "zero-click" pour exfiltrer des données via Copilot.

**Recommandations :**
*   **Application immédiate :** Déployer les mises à jour de sécurité de mars 2026 sur tous les systèmes Windows, SQL Server et environnements Azure concernés.
*   **Gestion des accès :** Étant donné le nombre élevé de failles d'élévation de privilèges, limiter les droits des utilisateurs locaux et surveiller les processus système critiques.
*   **Adoption des hotpatchs :** Pour les entreprises utilisant Microsoft Intune, préparer la transition vers le mode de mise à jour "hotpatch" activé par défaut à partir de mai 2026 pour réduire la fenêtre d'exposition.

---
[Source](https://thehackernews.com/2026/03/microsoft-patches-84-flaws-in-march.html){:target="_blank"}
