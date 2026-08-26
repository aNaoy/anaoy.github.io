---
title: 'FBI Disrupts China-Linked QTFY Infrastructure Used to Steal Data From U.S. Organizations'
date: 2026-08-26
permalink: /posts/2026/08/26/fbi-disrupts-china-linked-qtfy-infrastructure-used-to-steal-data-from-us-organizations/
tags:
- veille-cyber
- hackernews
---
### Démantèlement de l'infrastructure de cyberespionnage chinoise "QTFY"

Le FBI et le ministère de la Justice américain ont neutralisé deux plateformes majeures, **QScan** et **QTRouter**, opérées par le groupe chinois **QTFY**. Cette infrastructure agissait comme un "quartier-maître" numérique, permettant à des acteurs étatiques chinois de cibler des infrastructures critiques (NASA, Réserve fédérale, départements de l'Énergie, de la Justice, etc.) tout en masquant l'origine géographique de leurs intrusions.

**Points clés :**
*   **Mode opératoire :** QScan scanne et infecte des appareils IoT à travers le monde pour les intégrer à QTRouter.
*   **Obfuscation :** QTRouter utilise un réseau de serveurs relais et de connexions par procuration (proxy) pour faire transiter le trafic malveillant via des adresses IP locales, rendant la détection extrêmement complexe.
*   **Industrialisation :** QTFY opère via une entreprise nommée *Nanjing Xinjiuwei Network Technology*, collaborant avec le MSS et l'APL chinois pour fournir des outils d'intrusion et un accès aux réseaux victimes.

**Vulnérabilités exploitées :**
L'attaquant exploite une vaste gamme de vulnérabilités pour l'accès initial, incluant :
*   **Zero-day :** CVE-2024-8190, CVE-2024-8963, CVE-2024-9380 (Ivanti CSA).
*   **N-day notables :**
    *   Fortinet SSL-VPN : CVE-2018-13379
    *   Citrix ADC : CVE-2019-19781
    *   Microsoft Exchange : CVE-2021-26855
    *   F5 BIG-IP : CVE-2020-5902
    *   Apache Log4j : CVE-2021-44228
    *   Atlassian Confluence : CVE-2023-22515
    *   Check Point Quantum : CVE-2024-24919
    *   CrushFTP : CVE-2025-31161
    *   BeyondTrust : CVE-2026-1731

**Recommandations :**
*   **Gestion des correctifs :** Appliquer immédiatement les mises à jour de sécurité pour toutes les appliances de périphérie (VPN, passerelles, serveurs d'accès distant) citées ci-dessus.
*   **Sécurisation IoT :** Isoler les appareils IoT sur des réseaux distincts (segmentation) et désactiver les services de gestion à distance non nécessaires.
*   **Surveillance réseau :** Ne pas se fier uniquement aux blocages par géolocalisation IP. Privilégier une analyse comportementale du trafic pour détecter des anomalies dans les connexions entrantes (modèles de "proxy chaining").
*   **Hygiène des identifiants :** Auditer régulièrement les accès distants et les web shells persistants, car les attaquants utilisent des identifiants légitimes volés pour maintenir leur présence.

---
[Source](https://thehackernews.com/2026/08/fbi-disrupts-china-linked-qtfy.html){:target="_blank"}
