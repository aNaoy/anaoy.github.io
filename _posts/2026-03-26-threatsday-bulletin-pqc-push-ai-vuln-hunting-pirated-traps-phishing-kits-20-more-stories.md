---
title: 'ThreatsDay Bulletin: PQC Push, AI Vuln Hunting, Pirated Traps, Phishing Kits & 20 More Stories'
date: 2026-03-26
permalink: /posts/2026/03/26/threatsday-bulletin-pqc-push-ai-vuln-hunting-pirated-traps-phishing-kits-20-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces : Cryptographie quantique, IA offensive et persistance des attaquants

Le paysage cyber actuel est marqué par une résilience accrue des infrastructures malveillantes face aux démantèlements et une exploitation croissante des outils légitimes (logiciels piratés, services cloud, RMM) pour dissimuler des activités malveillantes.

#### Points clés
*   **Migration post-quantique :** Google accélère sa transition vers la cryptographie post-quantique (PQC) avec une échéance fixée à 2029, intégrant l'algorithme ML-DSA dans Android 17 pour sécuriser le démarrage et l'authentification.
*   **IA et vulnérabilités :** GitHub intègre l'IA dans ses outils de sécurité pour identifier des failles complexes que l'analyse statique traditionnelle ne détecte pas.
*   **Résilience des réseaux criminels :** Le démantèlement de plateformes de "Phishing-as-a-Service" (ex: Tycoon2FA) ne constitue qu'une entrave temporaire ; les infrastructures sont rapidement restaurées avec les mêmes tactiques.
*   **Espionnage et infiltration :** Des acteurs étatiques (DPRK, Sandworm, APT-Q-27) utilisent des techniques avancées comme le *DLL side-loading*, le vol de session, et même l'infiltration via des "travailleurs informatiques" synthétiques.
*   **Économie de la fraude :** Les "téléphones cloud" (fermes d'emulateurs Android) sont massivement utilisés pour le blanchiment d'argent, le vol de comptes bancaires (ATO/APP) et la manipulation de reviews/rankings.

#### Vulnérabilités et vecteurs d'attaque
*   **Keenadu (Backdoor firmware) :** Infection au niveau du firmware sur divers appareils Android bas coûts (500+ appareils compromis).
*   **ClawHub :** Vulnérabilité de contrôle d'accès permettant l'inflation artificielle des compteurs de téléchargement (escalade de privilèges sur les métriques).
*   **Services RMM détournés :** Utilisation de logiciels légitimes (Datto, LogMeIn, ScreenConnect) via de faux liens de mise à jour pour prendre le contrôle total des postes.
*   **Supply Chain :** Injections malveillantes dans des packages npm (typosquatting) pour voler des clés privées crypto.
*   **Obsolescence :** Plus de 511 000 serveurs IIS en fin de vie, dont 227 000 sans aucune mise à jour de sécurité (ESU).

#### Recommandations
*   **Anticipation PQC :** Prioriser l'audit des protocoles de chiffrement et d'authentification pour préparer la transition vers les standards post-quantiques (ML-DSA).
*   **Renforcement des terminaux :** Ne pas se fier uniquement aux outils EDR standards ; surveiller les comportements anormaux liés aux utilitaires de gestion à distance (RMM) et aux scripts PowerShell.
*   **Hygiène logicielle :** Éviter impérativement le téléchargement de logiciels "crackés" ou piratés, vecteurs privilégiés de backdoors complexes (Tambur, Kalambur).
*   **Gestion de la surface d'exposition :** Identifier et mettre à jour ou isoler les serveurs IIS obsolètes qui ne reçoivent plus de correctifs.
*   **Sensibilisation accrue :** Former les équipes de support client (spécifiquement Web3) à la méfiance envers les fichiers transmis via chat et les liens de "réunion" pointant vers des domaines suspects.

---
[Source](https://thehackernews.com/2026/03/threatsday-bulletin-pqc-push-ai-vuln.html){:target="_blank"}
