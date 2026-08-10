---
title: 'IT threat evolution in Q2 2026. Non-mobile statistics'
date: 2026-08-10
permalink: /posts/2026/08/10/it-threat-evolution-in-q2-2026-non-mobile-statistics/
tags:
- veille-cyber
- securelist
---
### Évolution des menaces informatiques : Analyse du T2 2026

Le second trimestre 2026 a été marqué par une activité cybercriminelle intense, caractérisée par une professionnalisation des services de signature de malwares et l'exploitation active de vulnérabilités critiques.

#### Points clés
*   **Volume d'attaques :** Près de 400 millions d'attaques en ligne bloquées ; 16 millions d'objets malveillants identifiés localement.
*   **Ransomwares :** 2 538 nouvelles variantes découvertes. Le groupe **Qilin** s'impose comme le plus prolifique, suivi par Akira et DragonForce.
*   **Minage :** Recrudescence notable avec 6 067 nouvelles variantes de logiciels de minage détectées.
*   **Techniques d'évasion :** Utilisation croissante de machines virtuelles légitimes (QEMU) pour dissimuler des charges utiles et échapper à la détection.
*   **Menaces macOS :** Hausse des logiciels publicitaires et découverte du backdoor **FlutterShell**, capable de contourner la notarisation d'Apple.

#### Vulnérabilités exploitées
*   **CVE-2026-33825 (Windows/Microsoft Defender) :** Vulnérabilité d'élévation de privilèges locale activement exploitée par des groupes de ransomware.
*   **CVE-2026-50751 & CVE-2026-50752 (Check Point VPN) :** Exploitation zero-day affectant les accès distants et les protocoles de chiffrement legacy (IKEv1), liée aux activités du groupe Qilin.

#### Recommandations
1.  **Gestion des correctifs :** Appliquer immédiatement les mises à jour de sécurité pour les systèmes Windows (CVE-2026-33825) et les équipements réseau, notamment les solutions VPN Check Point.
2.  **Sécurité des terminaux :** Renforcer la surveillance des environnements virtualisés et des extensions de navigateurs/IDE, vecteurs privilégiés pour les campagnes de type "stealer".
3.  **Désactivation des protocoles obsolètes :** Abandonner l'usage du protocole IKEv1 pour les connexions VPN site-à-site afin de limiter les risques liés à la validation de certificats.
4.  **Protection réseau :** Maintenir une posture de défense stricte sur les services SSH et Telnet, cibles principales des botnets IoT comme Mirai.

---
[Source](https://securelist.com/malware-report-q2-2026-pc-iot-statistics/120960/){:target="_blank"}
