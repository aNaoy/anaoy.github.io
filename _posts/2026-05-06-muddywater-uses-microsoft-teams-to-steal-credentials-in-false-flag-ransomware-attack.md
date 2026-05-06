---
title: 'MuddyWater Uses Microsoft Teams to Steal Credentials in False Flag Ransomware Attack'
date: 2026-05-06
permalink: /posts/2026/05/06/muddywater-uses-microsoft-teams-to-steal-credentials-in-false-flag-ransomware-attack/
tags:
- veille-cyber
- hackernews
---
### Stratégie de « False Flag » : MuddyWater détourne Microsoft Teams

Le groupe de cyberespionnage étatique iranien **MuddyWater** (aussi connu sous les noms de Mango Sandstorm ou Seedworm) mène des cyberattaques sous fausse bannière en utilisant le cadre du « Ransomware-as-a-Service » (RaaS) **Chaos**. L’objectif n’est pas le chiffrement de données, mais l'espionnage, l'exfiltration et la persistance à long terme, tout en masquant leurs activités derrière une opération criminelle opportuniste.

#### Points clés
*   **Mode opératoire :** Utilisation de l'ingénierie sociale via Microsoft Teams. Les attaquants se font passer pour le support informatique et incitent les victimes à partager leur écran pour récolter des identifiants et contourner l'authentification multifacteur (MFA).
*   **Techniques de persistance :** Installation d'outils de gestion à distance (DWAgent, AnyDesk) et déploiement d'un cheval de Troie d'accès à distance (RAT) personnalisé nommé « Darkcomp » (masqué en processus *Microsoft WebView2*).
*   **Détournement de RaaS :** L'usage du nom « Chaos » et la menace d'extorsion servent de couverture pour ralentir les équipes de réponse aux incidents, qui se concentrent sur une menace ransomware classique plutôt que sur une intrusion persistante menée par un acteur étatique.
*   **Attribution :** Le lien avec MuddyWater est confirmé par l'utilisation d'un certificat de signature de code spécifique (attribué à « Donald Gay ») déjà utilisé dans leurs campagnes précédentes.

#### Vulnérabilités et vecteurs d'attaque
*   **Vecteur initial :** Phishing et ingénierie sociale via Microsoft Teams et Microsoft Quick Assist.
*   **Logiciels malveillants :** 
    *   `ms_upd.exe` (Stagecomp) : Collecte d'informations système.
    *   `game.exe` (Darkcomp) : RAT basé sur le projet *WebView2APISample*.
*   **Infrastructure C2 :** Communication via des fichiers de configuration chiffrés (`visualwincomp.txt`) et des serveurs distants.

#### Recommandations
*   **Sensibilisation :** Former les utilisateurs aux risques de partage d'écran avec des contacts non vérifiés sur Microsoft Teams, même s'ils prétendent être du support technique.
*   **Surveillance des outils d'administration :** Restreindre et surveiller strictement l'installation et l'usage d'outils de prise de contrôle à distance (AnyDesk, DWAgent, Quick Assist).
*   **Analyse comportementale :** Ne pas se limiter à la détection de signatures de ransomwares. Rechercher des comportements anormaux, tels que l'utilisation inhabituelle de `curl` ou l'exécution de processus suspects se faisant passer pour des composants système légitimes (ex: WebView2).
*   **Renforcement MFA :** Mettre en place des politiques de MFA résistantes au phishing, car l'interception en direct via partage d'écran reste un point faible critique.

---
[Source](https://thehackernews.com/2026/05/muddywater-uses-microsoft-teams-to.html){:target="_blank"}
