---
title: 'CrowdSec Says TanStack npm Attack Led to Copy of 170 Private GitHub Repositories'
date: 2026-09-19
permalink: /posts/2026/09/19/crowdsec-says-tanstack-npm-attack-led-to-copy-of-170-private-github-repositories/
tags:
- veille-cyber
- hackernews
---
### Fuite de données chez CrowdSec via une attaque de supply chain

L'entreprise de cybersécurité CrowdSec a révélé que 170 de ses dépôts GitHub privés ont été compromis en mai 2026. L'incident fait suite à une attaque par empoisonnement de paquets npm visant **TanStack**, ayant permis de voler les identifiants d'un ancien employé dont l'accès GitHub n'avait pas encore été révoqué.

**Points clés :**
*   **Origine :** Compromission d'un poste de travail via des paquets npm malveillants de TanStack, permettant l'exfiltration de jetons d'authentification.
*   **Données exposées :** Code source interne (console web, modèles de data science, algorithmes), adresses email de 83 utilisateurs et informations confidentielles sur 51 investisseurs datant de 2020.
*   **Impact limité :** CrowdSec affirme que son infrastructure de production et ses bases de données n'ont pas été compromises. Un jeton AWS SNS trouvé dans le code a été tenté d'être utilisé sans succès.
*   **Contexte :** D'autres entreprises comme Mistral AI et OpenAI ont également été victimes de la même campagne d'attaque sur les paquets TanStack.

**Vulnérabilité associée :**
*   **CVE-2026-45321 :** Attaque de la chaîne d'approvisionnement (supply chain) via des versions malveillantes de paquets npm TanStack, capable d'exfiltrer des clés SSH, des jetons GitHub et des identifiants cloud.

**Recommandations :**
*   **Gestion des accès :** Révoquer immédiatement les accès (GitHub, VPN, cloud) des employés quittant l'entreprise.
*   **Sécurité des terminaux :** Déployer systématiquement des solutions de protection (EDR/antivirus) sur les postes des développeurs manipulant du code source.
*   **Gestion des secrets :** Rotation proactive des clés API et jetons d'accès dès la détection d'une compromission potentielle sur une machine de développement.
*   **Vigilance supply chain :** Surveiller étroitement les dépendances open-source et auditer régulièrement les outils utilisés par les équipes techniques.

---
[Source](https://thehackernews.com/2026/09/crowdsec-says-tanstack-npm-attack-led.html){:target="_blank"}
