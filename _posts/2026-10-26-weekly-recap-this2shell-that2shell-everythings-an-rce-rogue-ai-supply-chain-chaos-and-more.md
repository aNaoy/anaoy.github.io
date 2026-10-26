---
title: '⚡ Weekly Recap: This2Shell, That2Shell, Everythings an RCE? Rogue AI, Supply Chain Chaos and More'
date: 2026-10-26
permalink: /posts/2026/10/26/weekly-recap-this2shell-that2shell-everythings-an-rce-rogue-ai-supply-chain-chaos-and-more/
tags:
- veille-cyber
- hackernews
---
### Recrudescence des vulnérabilités RCE et menaces sur la supply chain

La semaine a été marquée par une vague massive de vulnérabilités critiques de type exécution de code à distance (RCE), touchant des infrastructures largement déployées et exploitées activement par des attaquants.

#### Points clés
*   **Vague de "Shell" :** Multiplication des failles RCE (PHP2Shell, Node2Shell, Plex2Shell) permettant des prises de contrôle sans authentification.
*   **Risques liés à l'IA :** Manipulation d'agents IA (via des fichiers `AGENTS.md` malveillants), compromission de clés API et usage d'IA pour des attaques tactiques.
*   **Supply Chain :** Compromission de paquets Python (LiteLLM) via une clé maîtresse divulguée et arrêt de l'activité de certificats TLS par eMudhra suite à des clés privées trop faibles.
*   **Exploitation rapide :** Le délai entre la publication d'une vulnérabilité et son exploitation réelle est désormais réduit à environ 3 jours.

#### Vulnérabilités majeures identifiées
*   **PHP (PHP2Shell) :** CVE-2026-109618 et CVE-2026-109619.
*   **Google Brotli / Node.js (Node2Shell) :** CVE-2026-111497.
*   **GitLab :** CVE-2026-110264 (Score CVSS 10.0).
*   **Plex Media Server (Plex2Shell) :** CVE-2026-96652, CVE-2026-96654, CVE-2026-96655, CVE-2026-96656 (inclus au catalogue KEV de la CISA).
*   **Linux KSMBD :** ZDI-CAN-33774, ZDI-CAN-33549 (CVSS 9.0, correctifs en attente).
*   **Ruby (Onigmo) :** CVE-2026-89078, CVE-2026-93577, CVE-2026-97229, CVE-2026-110264.

#### Recommandations
1.  **Priorisation des correctifs :** Appliquer immédiatement les correctifs pour PHP, GitLab, Plex et les bibliothèques dépendantes de Brotli.
2.  **Gestion des secrets :** Révoquer et renouveler systématiquement toute clé API ou variable d'environnement exposée sur des dépôts publics ou potentiellement compromise.
3.  **Durcissement des systèmes :** Pour les serveurs KSMBD, restreindre l'usage des *namespaces* utilisateur non privilégiés et appliquer des profils `seccomp` stricts.
4.  **Sécurité des agents IA :** Ne pas accorder une confiance aveugle aux instructions contenues dans les fichiers de configuration (type `AGENTS.md`) et surveiller les accès des agents IA aux dossiers téléchargements.
5.  **Audit de surface :** Identifier les instances exposées de services critiques et isoler les systèmes ne pouvant pas être patchés immédiatement.

---
[Source](https://thehackernews.com/2026/10/weekly-recap-this2shell-that2shell.html){:target="_blank"}
