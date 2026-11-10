---
title: 'IT threat evolution in Q3 2026. Non-mobile statistics'
date: 2026-11-10
permalink: /posts/2026/11/10/it-threat-evolution-in-q3-2026-non-mobile-statistics/
tags:
- veille-cyber
- securelist
---
### Évolution des menaces informatiques : T3 2026

Au troisième trimestre 2026, l'activité cybercriminelle s'est intensifiée, marquée par une recrudescence des variantes de ransomwares et des attaques sophistiquées ciblant les vulnérabilités logicielles.

#### Points clés
*   **Volume d'attaques :** Plus de 311 millions d'attaques en ligne bloquées et 23 millions d'objets malveillants détectés localement.
*   **Ransomwares :** 4 470 nouvelles variantes identifiées (+50% par rapport au trimestre précédent). Le groupe **Qilin** reste le plus prolifique, suivi par "The Gentlemen" et le nouveau venu "Deadlock".
*   **Menaces macOS :** Hausse des attaques ciblant la chaîne d'approvisionnement (packages npm, PyPI, Rust) pour voler des secrets et des API, ainsi que la découverte de nouveaux malwares comme *PamStealer* et le backdoor *Overlord*.
*   **IoT :** Augmentation des attaques SSH (18,42% des sondages) et des sessions malveillantes via Telnet, notamment depuis le Pakistan, la Bulgarie et les Pays-Bas.

#### Vulnérabilités exploitées (CVE)
Les attaquants exploitent activement des failles permettant le contournement de l'authentification ou l'exécution de code à distance (RCE) :
*   **CVE-2026-0257 :** Contournement d'authentification sur les pare-feu Palo Alto Networks (utilisé par Qilin).
*   **CVE-2026-15409 / CVE-2026-15410 :** Passerelles d'accès distant SonicWall SMA1000.
*   **CVE-2026-45659 :** RCE sur Microsoft SharePoint Server.
*   **CVE-2026-59310 :** RCE non authentifié sur VMware vCenter.
*   **CVE-2026-63077 :** Contournement d'authentification sur JetBrains TeamCity permettant l'exécution de commandes système.
*   **CVE-2025-60710 & CVE-2025-14733 :** Élévation de privilèges (Windows) et RCE (WatchGuard).

#### Recommandations
*   **Gestion des vulnérabilités :** Appliquer en priorité les correctifs pour les CVE listées ci-dessus, particulièrement pour les équipements réseau (pare-feu, passerelles VPN) qui constituent des vecteurs d'entrée privilégiés.
*   **Sécurisation de la Supply Chain :** Auditer systématiquement les dépendances logicielles et les packages (npm, PyPI, Rust) avant leur intégration dans les environnements de développement.
*   **Durcissement de l'accès distant :** Désactiver les services Telnet et restreindre strictement l'accès SSH aux adresses IP connues.
*   **Protection des endpoints :** Maintenir des solutions antivirus à jour capables de détecter les comportements suspects (heuristique) pour contrer les variantes de ransomwares en constante évolution.

---
[Source](https://securelist.com/malware-report-q3-2026-pc-iot-statistics/121843/){:target="_blank"}
