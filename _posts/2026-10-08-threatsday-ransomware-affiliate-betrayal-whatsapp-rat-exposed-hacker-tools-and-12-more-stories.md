---
title: 'ThreatsDay: Ransomware Affiliate Betrayal, WhatsApp RAT, Exposed Hacker Tools and 12 More Stories'
date: 2026-10-08
permalink: /posts/2026/10/08/threatsday-ransomware-affiliate-betrayal-whatsapp-rat-exposed-hacker-tools-and-12-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces : De la chaîne d’approvisionnement aux failles critiques

L'actualité cybersécurité récente révèle une diversification des méthodes d'attaque, allant de la compromission de la supply chain logicielle à l'abus d'outils légitimes, tout en soulignant une négligence croissante, tant chez les victimes que chez les cybercriminels eux-mêmes.

**Points clés :**
*   **Supply Chain :** Multiplication des extensions VS Code et packages (npm, RubyGems) malveillants visant les développeurs pour exfiltrer des identifiants ou établir des accès distants (reverse shells).
*   **Menaces hybrides :** Utilisation croissante de l'IA (injection de prompts dans des emails de phishing) et abus de services légitimes (Power BI) pour crédibiliser les attaques.
*   **Infrastructure de malware :** Le framework *BraZetsu* et le RAT *VulcanRAT207* démontrent une sophistication accrue dans l'évasion des systèmes de sécurité via des techniques de "Bring Your Own Vulnerable Driver" (BYOVD).
*   **Fragilité industrielle :** Un manque critique de préparation à la cryptographie post-quantique (PQC) dans les dispositifs médicaux (IoMT) et OT.
*   **Sabotage et trahison :** Des cas d'insiders malveillants et de conflits internes au sein de groupes de ransomware (vol de profits par des affiliés) témoignent de l'instabilité de l'écosystème criminel.

**Vulnérabilités identifiées :**
*   **Upload de fichiers :** Faille dans des plateformes de gestion permettant l'exécution de *web shells*.
*   **Cookies de session :** Usage de secrets codés en dur et d'identifiants prédictibles (CUID) permettant l'usurpation de compte sans authentification.
*   **MSSQL :** Abus de la fonctionnalité `xp_cmdshell` pour l'exécution de commandes système et l'exfiltration de données via les résultats de requêtes.

**Recommandations :**
*   **Audit des dépendances :** Vérifier systématiquement l'intégrité des packages tiers avant déploiement et surveiller les comportements suspects lors de l'installation (appels réseau inattendus).
*   **Sécurisation des sessions :** Proscrire l'utilisation d'identifiants prédictibles ou de clés secrètes statiques pour la signature des jetons de session. Privilégier des identifiants aléatoires et des secrets dynamiques.
*   **Durcissement MSSQL :** Désactiver `xp_cmdshell` s'il n'est pas strictement nécessaire et restreindre les privilèges des comptes de service.
*   **Veille PQC :** Prioriser la mise à jour vers TLS 1.3 pour les équipements critiques, étape indispensable pour une future transition vers la cryptographie post-quantique.
*   **Protection des endpoints :** Adopter des solutions EDR capables de détecter les techniques de *process injection* (type PoolParty) et les pilotes vulnérables utilisés dans les attaques BYOVD.

---
[Source](https://thehackernews.com/2026/10/threatsday-ransomware-affiliate.html){:target="_blank"}
