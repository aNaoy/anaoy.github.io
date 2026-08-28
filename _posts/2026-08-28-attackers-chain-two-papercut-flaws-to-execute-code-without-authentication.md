---
title: 'Attackers Chain Two PaperCut Flaws to Execute Code Without Authentication'
date: 2026-08-28
permalink: /posts/2026/08/28/attackers-chain-two-papercut-flaws-to-execute-code-without-authentication/
tags:
- veille-cyber
- hackernews
---
### Exploitation critique des serveurs PaperCut : RCE par chaînage de vulnérabilités

Des attaquants exploitent activement deux failles critiques dans les solutions PaperCut NG et MF pour prendre le contrôle total de serveurs distants sans authentification. En enchaînant ces vulnérabilités, les cybercriminels contournent les contrôles d'accès pour modifier la configuration du serveur et exécuter du code Java arbitraire.

**Points clés :**
*   **Mode opératoire :** L'attaque commence par un contournement de l'authentification (via CVE-2026-81578), permettant de modifier des fichiers de configuration pour déclencher l'exécution de code (via CVE-2026-82078).
*   **Activités malveillantes :** Les attaquants effectuent une reconnaissance système (identification de l'utilisateur, version de l'OS, liste des processus) et déploient des fichiers Java temporaires pour exfiltrer des données avant d'effacer leurs traces (logs).
*   **État de la menace :** Malgré la publication de correctifs d'urgence, des chercheurs ont identifié des tentatives de contournement de ces mêmes patchs, soulignant la persistance du risque.

**Vulnérabilités identifiées :**
*   **CVE-2026-82078 (Score CVSS : 9.4) :** Chargement dynamique de classes non sécurisé dans les utilitaires de connexion à la base de données, permettant l'exécution de code arbitraire.
*   **CVE-2026-81578 (Score CVSS : 8.8) :** Contrôle d'accès défaillant dans l'interface de gestion web, permettant à un attaquant non authentifié de déclencher des actions administratives backend.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs les plus récents fournis par PaperCut, qui incluent des mesures de durcissement supplémentaires.
*   **Restriction d'accès :** Supprimer l'exposition directe du serveur sur Internet. Restreindre l'accès à l'interface d'administration via une liste d'adresses IP de confiance ou un VPN.
*   **Surveillance :** Rechercher des indicateurs de compromission dans les logs, notamment l'erreur spécifique : `"Database error looking up cardID: VALUES CAST"`.

---
[Source](https://thehackernews.com/2026/08/attackers-chain-two-papercut-flaws-to.html){:target="_blank"}
