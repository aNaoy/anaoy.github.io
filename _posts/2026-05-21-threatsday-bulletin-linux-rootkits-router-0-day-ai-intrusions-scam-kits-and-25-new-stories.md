---
title: 'ThreatsDay Bulletin: Linux Rootkits, Router 0-Day, AI Intrusions, Scam Kits and 25 New Stories'
date: 2026-05-21
permalink: /posts/2026/05/21/threatsday-bulletin-linux-rootkits-router-0-day-ai-intrusions-scam-kits-and-25-new-stories/
tags:
- veille-cyber
- hackernews
---
### État des menaces : L'industrialisation des vecteurs d'attaque

La semaine a été marquée par une intensification des cyberattaques exploitant des composants de confiance, des erreurs de configuration et l'intégration accélérée de l'intelligence artificielle (IA) dans les opérations malveillantes.

#### Points clés
* **IA générative et agentique :** Les attaquants utilisent l'IA pour automatiser la reconnaissance, générer des outils de piratage à la volée (contournant les signatures classiques) et concevoir des campagnes de spear-phishing ultra-personnalisées.
* **Exploitation de la confiance :** Le motif récurrent est l'utilisation détournée d'outils légitimes (LOLBins, services cloud, dépôts de code) pour se fondre dans le trafic administratif.
* **Complexité des vecteurs :** L'usage de stéganographie, de scripts PowerShell polymorphes et de "Living-off-the-Land" complique la détection.
* **Pwn2Own 2026 :** 47 vulnérabilités zero-day exploitées sur des cibles majeures (Windows, Linux, VMware, NVIDIA).

#### Vulnérabilités critiques
* **CVE-2026-45793 (Score CVSS 7.5) :** Fuite de jetons (GitHub Actions tokens) dans les journaux d'erreurs lors de l'utilisation de Composer (gestionnaire PHP).
* **CVE-2026-8631 (Score CVSS 9.3) :** Dépassement de tampon critique dans HPLIP, exposant les serveurs d'impression et les systèmes Linux à une exécution de code arbitraire à distance (RCE).

#### Recommandations
1. **Sécuriser les outils d'IA :** Appliquer des contrôles d'accès stricts sur les agents IA en entreprise pour éviter les privilèges excessifs et le contournement des garde-fous de sécurité.
2. **Gestion des dépendances :** Mettre à jour immédiatement Composer (versions 2.9.8 / 2.2.28) et auditer régulièrement les bibliothèques open-source pour détecter le typosquatting (ex: module Go malveillant `decimal`).
3. **Hygiène des infrastructures :** 
    * Appliquer les correctifs pour HPLIP sur tous les systèmes Linux.
    * Désactiver temporairement les workflows GitHub Actions utilisant des commandes Composer en attendant la mise à jour.
4. **Surveillance des comportements :** Ne pas ignorer les alertes "ennuyeuses" ou familières ; les attaquants actuels utilisent souvent des techniques persistantes (comme le rootkit *OrBit* sur Linux) ou des outils hérités (MSHTA) qui déclenchent des signaux faibles négligés par les équipes de sécurité.
5. **Gestion des accès Cloud :** Renforcer la surveillance des configurations Azure/AWS pour détecter l'abus de fonctionnalités légitimes (SSPR, gestion de comptes) plutôt que de se concentrer uniquement sur les malwares classiques.

---
[Source](https://thehackernews.com/2026/05/threatsday-bulletin-linux-rootkits.html){:target="_blank"}
