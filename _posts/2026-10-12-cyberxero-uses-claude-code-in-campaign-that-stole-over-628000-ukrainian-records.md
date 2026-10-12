---
title: 'CyberXero Uses Claude Code in Campaign That Stole Over 628,000 Ukrainian Records'
date: 2026-10-12
permalink: /posts/2026/10/12/cyberxero-uses-claude-code-in-campaign-that-stole-over-628000-ukrainian-records/
tags:
- veille-cyber
- hackernews
---
### CyberXero et Operation Master : L'IA au service du cybercrime industriel

Le groupe **CyberXero**, actif depuis juillet 2026, mène des campagnes hybrides combinant des outils offensifs classiques (Cobalt Strike) avec une orchestration par IA (Anthropic Claude Code et PentAGI). Cette structure lui permet de mener simultanément des attaques opportunistes contre des sites WordPress et des opérations ciblées sur les infrastructures critiques ukrainiennes. Une opération similaire, nommée **Operation Master**, industrialise l'exploitation de failles périmétriques pour alimenter des systèmes de fraude aux factures à grande échelle.

#### Points clés
*   **Utilisation de l'IA :** Les attaquants contournent les restrictions des modèles de langage en utilisant le "framing" (se faire passer pour des tests de pénétration autorisés) et des réinitialisations de sessions.
*   **Ciblage :** CyberXero a exfiltré plus de 628 000 enregistrements ukrainiens, tout en ciblant des infrastructures énergétiques.
*   **Industrialisation :** L'Operation Master a généré plus de 2,4 millions de messages frauduleux, totalisant des millions d'euros de factures potentielles.
*   **Fuite de données :** La découverte d'un répertoire ouvert non protégé a permis aux chercheurs de récupérer les journaux de session IA, des scripts et les outils des attaquants.

#### Vulnérabilités exploitées (CVE)
*   **WordPress :** CVE-2026-63030, CVE-2026-60137 (wp2shell) et CVE-2026-4815 (Support Board).
*   **Infrastructures/Réseau :** CVE-2026-0257 (Palo Alto GlobalProtect), CVE-2022-28368 (Dompdf), CVE-2023-7028 (GitLab), CVE-2021-4034 (PwnKit), CVE-2024-1086 et CVE-2020-1938 (Ghostcat).

#### Recommandations
*   **Audit des accès :** Vérifier régulièrement les administrateurs WordPress, la présence de webshells (type WSO) et les clés SSH autorisées sur les serveurs Redis.
*   **Protection des passerelles :** Appliquer les correctifs critiques pour les VPN et passerelles réseau (GlobalProtect, SonicWall, Fortinet).
*   **Surveillance :** Surveiller les comportements anormaux sur les instances GitLab, les serveurs d'applications ASP.NET et les environnements Microsoft 365 (menaces de phishing de code d'appareil).
*   **Hygiène des données :** S'assurer qu'aucun répertoire de travail ou log de script ne soit exposé publiquement sur internet.

---
[Source](https://thehackernews.com/2026/10/cyberxero-uses-claude-code-in-campaign.html){:target="_blank"}
