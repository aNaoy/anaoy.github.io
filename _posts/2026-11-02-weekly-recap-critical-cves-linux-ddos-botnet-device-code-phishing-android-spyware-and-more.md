---
title: '⚡ Weekly Recap: Critical CVEs, Linux DDoS Botnet, Device-Code Phishing, Android Spyware and More'
date: 2026-11-02
permalink: /posts/2026/11/02/weekly-recap-critical-cves-linux-ddos-botnet-device-code-phishing-android-spyware-and-more/
tags:
- veille-cyber
- hackernews
---
### Rétrospective hebdomadaire : Menaces critiques et cyber-attaques

Cette semaine a été marquée par une recrudescence d'attaques exploitant des vecteurs simples (ingénierie sociale, extensions compromises, appareils mal sécurisés) ainsi que des campagnes sophistiquées ciblant les infrastructures critiques et les crypto-actifs.

#### Points clés
*   **Vol record de cryptomonnaies :** Le groupe nord-coréen *TraderTraitor* a dérobé 6,43 milliards de dollars sur Binance, marquant le plus gros vol de l'histoire du secteur.
*   **Infrastructures d'attaques :** Le groupe *Volt Typhoon* utilise le réseau "Silent Train", une chaîne tournante d'appareils compromis pour dissimuler ses attaques sur des infrastructures critiques.
*   **Supply Chain et extensions :** Une extension Claude Code malveillante a été détectée sur le marketplace Cursor, compromettant environ 5 000 utilisateurs via une porte dérobée SSH. Parallèlement, 319 extensions Chrome malveillantes ont été supprimées pour détournement de recherche.
*   **Espionnage et fraude :** Le spyware Android *uCreator* clone des comptes de messagerie et de paiement, tandis que les campagnes de phishing via Microsoft Teams se multiplient pour obtenir des accès distants (Quick Assist).
*   **IA et automatisation :** Le ransomware *Aur0ra* utilise l'IA pour automatiser ses phases post-exploitation, contournant les protections en se faisant passer pour des tests de sécurité.

#### Vulnérabilités majeures (CVE)
De nombreuses vulnérabilités ont été signalées cette semaine, nécessitant une attention immédiate :
*   **Wasmtime :** CVE-2026-115889, CVE-2026-115893
*   **Okta (Access Gateway) :** CVE-2026-115547
*   **Apache Kafka :** CVE-2026-114349, CVE-2026-111551
*   **Google Chrome :** CVE-2026-118306, CVE-2026-106378
*   **Linux Kernel :** CVE-2026-98432
*   **Veeam :** CVE-2026-107239, CVE-2026-107238
*   *Note : Des correctifs sont également en cours pour Apache Tomcat, Drupal, HashiCorp consul-k8s, et une longue liste de produits ASUS.*

#### Recommandations
1.  **Gestion des correctifs :** Prioriser l'application des patchs pour les CVE listées ci-dessus, en commençant par les systèmes exposés sur Internet (Okta, Kafka, Chrome).
2.  **Sécurité des appareils IoT/SOHO :** Modifier immédiatement les identifiants par défaut (ex: Telnet root/vide) pour éviter l'enrôlement dans des botnets comme *Kairos*.
3.  **Vigilance sur la chaîne d'approvisionnement :** Vérifier les extensions tierces installées dans les environnements de développement (type VS Code/Cursor).
4.  **Sensibilisation :** Alerter les utilisateurs sur les campagnes de phishing utilisant des appels "IT" factices via Microsoft Teams et sur les dangers du "device code phishing".
5.  **Audit des secrets :** Vérifier l'intégrité des workflows CI/CD (ex: GitHub Actions) pour détecter toute extraction illicite de secrets (campagne *Gheist*).

---
[Source](https://thehackernews.com/2026/11/weekly-recap-critical-cves-linux-ddos.html){:target="_blank"}
