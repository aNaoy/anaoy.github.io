---
title: 'Microsoft August 2025 Patch Tuesday Fixes Kerberos Zero-Day Among 111 Total New Flaws'
date: 2025-08-13
permalink: /posts/2025/08/13/microsoft-august-2025-patch-tuesday-fixes-kerberos-zero-day-among-111-total-new-flaws/
tags:
- veille-cyber
- hackernews
---
### Mise à jour de sécurité Microsoft : correction d'une faille Kerberos critique et 110 autres vulnérabilités

Microsoft a publié 111 correctifs de sécurité ce mois-ci, dont un zero-day déjà connu publiquement. Ces mises à jour visent à corriger diverses failles critiques et importantes dans ses produits.

**Points Clés :**

*   111 vulnérabilités corrigées au total.
*   16 vulnérabilités classées comme critiques, 92 importantes, 2 modérées et 1 faible.
*   Les vulnérabilités les plus courantes concernent l'escalade de privilèges (44), l'exécution de code à distance (35) et la divulgation d'informations (18).
*   16 vulnérabilités supplémentaires ont été corrigées dans le navigateur Edge basé sur Chromium.

**Vulnérabilités Notables :**

*   **CVE-2025-53779 (score CVSS 7.2) :** Escalade de privilèges dans Kerberos de Windows. Permet à un attaquant avec des privilèges suffisants de compromettre un domaine Active Directory en abusant des objets de compte de service gérés délégués (dMSA). Connue sous le nom de "BadSuccessor", elle nécessite un contrôle préalable sur deux attributs spécifiques du dMSA pour être exploitée. Une exploitation réussie peut permettre à un attaquant de passer de droits administratifs limités à un contrôle total du domaine, voire d'affecter d'autres domaines dans des scénarios de chaîne d'approvisionnement.
*   **CVE-2025-53786 (score CVSS 8.0) :** Escalade de privilèges affectant les déploiements hybrides de Microsoft Exchange Server.
*   **CVE-2025-53767 (score CVSS 10.0) :** Vulnérabilité d'élévation de privilèges dans Azure OpenAI.
*   **CVE-2025-53766 (score CVSS 9.8) :** Vulnérabilité d'exécution de code à distance dans GDI+. Nécessite l'ouverture d'un fichier spécialement conçu par un utilisateur.
*   **CVE-2025-50165 (score CVSS 9.8) :** Vulnérabilité d'exécution de code à distance dans le composant graphique de Windows.
*   **CVE-2025-50154 (score CVSS 6.5) :** Vulnérabilité de divulgation de hash NTLM, contournant une correction précédente. Permet à un attaquant d'extraire des hashs NTLM sans interaction utilisateur, ouvrant la voie à des attaques hors ligne ou des attaques par relais.
*   Une vulnérabilité dans un composant basé sur Rust du noyau Windows peut provoquer un crash système, entraînant un redémarrage forcé.

**Recommandations :**

*   Appliquer immédiatement les mises à jour de sécurité publiées par Microsoft.
*   Les vulnérabilités touchant les services cloud Azure OpenAI, Azure Portal et Microsoft 365 Copilot BizChat sont déjà corrigées et ne nécessitent aucune action de la part des clients.
*   Une vigilance continue et des correctifs proactifs sont essentiels pour maintenir l'intégrité des systèmes.

---
[Source](https://thehackernews.com/2025/08/microsoft-august-2025-patch-tuesday.html){:target="_blank"}
