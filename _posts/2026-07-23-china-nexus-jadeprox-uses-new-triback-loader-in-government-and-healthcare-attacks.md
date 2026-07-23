---
title: 'China-Nexus JadeProx Uses New TriBack Loader in Government and Healthcare Attacks'
date: 2026-07-23
permalink: /posts/2026/07/23/china-nexus-jadeprox-uses-new-triback-loader-in-government-and-healthcare-attacks/
tags:
- veille-cyber
- hackernews
---
### Opérations du groupe JadeProx : Analyse du chargeur TriBack

Le groupe d'acteurs « JadeProx », lié à la Chine, mène des campagnes d'intrusion ciblant des secteurs critiques (gouvernement, santé, éducation) en Asie et en Amérique latine. L'opération repose sur l'utilisation d'un nouveau chargeur (loader) malveillant baptisé **TriBack**, exploitant des techniques de *DLL sideloading* pour déployer des frameworks de post-exploitation comme AdaptixC2 ou le backdoor Beagle.

**Points clés :**
*   **Vecteurs d'attaque :** Utilisation de webshells sur des interfaces de gestion Java exposées et campagnes de spear-phishing (usurpation de sites comme Claude AI).
*   **Technique TriBack :** Le chargeur utilise des fichiers DLL légitimes signés associés à des charges utiles chiffrées. Il exécute du code malveillant via des appels API peu surveillés par les EDR (`InitOnceExecuteOnce`, `EtwpCreateEtwThread`).
*   **Scanning massif :** Le groupe utilise l'outil Nuclei pour scanner des milliers d'URL à la recherche de vulnérabilités critiques connues (CVSS 9.8).

**Vulnérabilités exploitées :**
*   **CVE-2018-11511** (ASUSTOR ADM)
*   **CVE-2021-24139** (Plugin WordPress 10Web Photo Gallery)
*   **CVE-2021-31755** (Routeurs Tenda AC11)
*   **CVE-2021-32305** (WebSVN)

**Recommandations :**
*   **Surveillance du Sideloading :** Identifier les exécutables signés s'exécutant depuis des répertoires temporaires ou de démarrage (Startup) accompagnés de fichiers `.dat` ou `.log` suspects.
*   **Chasse aux menaces :** Rechercher la présence de bibliothèques détournées (`hostfxr.dll`, `avk.dll`, `MpClient.dll`) ou de dossiers atypiques.
*   **Filtrage réseau :** Bloquer les domaines liés à la campagne (ex: `claude-pro[.]com`, `update-trellix[.]com`, `update-crowdstrike[.]com`) et surveiller les connexions vers l'IP `43.106.71.28`.
*   **Hygiène logicielle :** Prioriser le patch des vulnérabilités critiques (score 9.8) sur les systèmes exposés à Internet, en particulier les applications Java et les équipements réseaux.

---
[Source](https://thehackernews.com/2026/07/china-nexus-jadeprox-uses-new-triback.html){:target="_blank"}
