---
title: 'Ransom Busters Claims It Hacked Ransomware Servers, Asks Victims for Up to $60,000'
date: 2026-08-18
permalink: /posts/2026/08/18/ransom-busters-claims-it-hacked-ransomware-servers-asks-victims-for-up-to-60000/
tags:
- veille-cyber
- hackernews
---
### Menaces d'extorsion et tactiques émergentes dans l'écosystème ransomware

Le paysage de la cyber-extorsion évolue avec l'émergence d'acteurs opportunistes tels que « Ransom Busters », qui contactent proactivement des victimes de ransomwares pour leur proposer, moyennant 20 000 à 60 000 $, la suppression des données exfiltrées. Cette pratique est considérée comme une supercherie par les experts, visant à extorquer des fonds supplémentaires sans aucune garantie de sécurité. Parallèlement, des groupes comme UNC6671 industrialisent le « vishing » (phishing vocal) pour voler des identifiants et cibler de grandes organisations, générant plus de 8 millions de dollars de gains.

**Points clés :**
*   **Fragmentation du secteur :** Le nombre de groupes actifs a fortement augmenté, passant de 71 à 93 en un trimestre, avec une stratégie orientée vers l'exfiltration de données plutôt que sur le chiffrement seul.
*   **Tactiques de dissimulation :** Les attaquants abusent d'outils légitimes (Cloud, outils d'administration à distance, binaires signés) pour se fondre dans le trafic réseau normal.
*   **Diversification des méthodes :** Certains groupes, à l'instar de CRPx0, combinent ransomware, Hacking-as-a-Service (HaaS) et outils de vol de cryptomonnaies (« clipper »).
*   **Obsolescence des solutions miracles :** Aucun paiement ne garantit la suppression réelle des données volées.

**Vulnérabilités et vecteurs d'attaque :**
*   **Accès initiaux :** Exploitation récurrente de VPN (ex: SonicWall) et techniques de *credential harvesting*.
*   **Outils identifiés :** Utilisation de *SoftPerfect Network Scanner* pour la reconnaissance, *s5cmd* pour l'exfiltration vers AWS, et scripts PowerShell pour déployer des outils RMM (Remote Monitoring and Management).
*   **Indicateurs techniques :** Création récurrente de comptes backdoors locaux avec le mot de passe `Numlock!123` et persistance du nom d'hôte `DESKTOP-BBETH6K`.
*   **Contournement de la sécurité :** Tentatives de désactivation des EDR (Endpoint Detection and Response) en forçant le redémarrage des systèmes en "Mode sans échec avec prise en charge réseau".

**Recommandations :**
*   **Ne pas payer :** Ne jamais traiter avec des entités se présentant comme des « sauveurs » après une attaque ; il s'agit presque systématiquement d'une escroquerie.
*   **Sécurisation des accès :** Implémenter une authentification multifacteur (MFA) robuste, particulièrement pour les services VPN et les accès distants.
*   **Surveillance renforcée :** Détecter les anomalies de comportement des outils d'administration légitimes (RMM, PowerShell) et les tentatives inhabituelles de redémarrage système.
*   **Veille stratégique :** Surveiller les sites de fuite de données et maintenir une politique de gestion des correctifs rigoureuse pour contrer les tactiques de « big game hunting ».

---
[Source](https://thehackernews.com/2026/08/ransom-busters-claims-it-hacked.html){:target="_blank"}
