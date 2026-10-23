---
title: 'Russia-Linked Hackers Used New Mesh Network Backdoor in Destructive Ukraine Attack'
date: 2026-10-23
permalink: /posts/2026/10/23/russia-linked-hackers-used-new-mesh-network-backdoor-in-destructive-ukraine-attack/
tags:
- veille-cyber
- hackernews
---
### Collaboration cyber-offensive : Sandworm et UAC-0099 infiltrent l'Ukraine via Yggdrasil

Le groupe étatique russe Sandworm a collaboré avec l'acteur de menace UAC-0099 pour mener une attaque destructrice par effacement de données contre une entreprise logistique ukrainienne en 2025. Cette opération illustre une tendance croissante de coopération entre groupes alignés sur la Russie, où UAC-0099 assure l'accès initial et la reconnaissance, tandis que Sandworm exécute la phase finale de sabotage.

**Points clés :**
*   **Mode opératoire :** UAC-0099 obtient un accès initial via du hameçonnage (spear-phishing) déployant le téléchargeur *MATCHBOIL* et la porte dérobée *MATCHWOK*.
*   **Innovation technique :** Utilisation de la nouvelle porte dérobée **MythicRatatoskr**, capable de communiquer via le réseau maillé (mesh network) décentralisé **Yggdrasil** pour accroître la résilience et la furtivité du serveur de commande et de contrôle (C2).
*   **Charge finale :** Sandworm a pris le relais après deux mois pour déployer un utilitaire d'effacement de données basé sur *SDelete* via les politiques de groupe Active Directory (GPO).
*   **Portée :** Bien que l'attaque visât Windows, la présence de références à "crond" dans le code suggère l'existence d'une variante Linux de MythicRatatoskr.

**Vulnérabilités et vecteurs d'attaque :**
*   **Vecteur d'entrée :** Hameçonnage ciblé par courriel (pièce jointe malveillante).
*   **CVE :** Aucune CVE spécifique n'est mentionnée ; l'attaque repose sur des malwares personnalisés (MATCHWOK, MythicRatatoskr) et l'usage détourné d'outils légitimes (SDelete).

**Recommandations :**
*   **Surveillance réseau :** Surveiller les connexions inhabituelles vers le réseau Yggdrasil au sein de l'infrastructure d'entreprise.
*   **Durcissement Active Directory :** Restreindre les privilèges permettant le déploiement de logiciels via GPO et auditer régulièrement les changements de politiques.
*   **Défense contre le hameçonnage :** Renforcer la sensibilisation des utilisateurs et implémenter des solutions de filtrage de courriels avancées.
*   **Détection d'anomalies :** Rechercher des comportements suspects de type "exécution différée" (délai de 10 minutes au démarrage observé) et des activités anormales de reverse SOCKS5.

---
[Source](https://thehackernews.com/2026/10/russian-linked-hackers-used-new-mesh.html){:target="_blank"}
