---
title: 'Hackers abuse ViPNet software to target Russian govt agencies'
date: 2026-07-19
permalink: /posts/2026/07/19/hackers-abuse-vipnet-software-to-target-russian-govt-agencies/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne HelloNet : Détournement du logiciel ViPNet

La campagne "HelloNet" cible des organisations russes stratégiques (gouvernement, énergie, transports) en exploitant le mécanisme de mise à jour de la suite de sécurité ViPNet (InfoTeCS). Bien que l'infrastructure officielle ne semble pas compromise, les attaquants parviennent à injecter une DLL malveillante dans le répertoire local du logiciel pour obtenir des privilèges élevés et maintenir une persistance.

**Points clés :**
*   **Méthode d'attaque :** Utilisation du processus légitime `itcsrvup64.exe` pour charger une bibliothèque dynamique malveillante (`wtsapi32.dll` ou "HelloInjector") par "DLL sideloading".
*   **Capacités :** Les charges utiles permettent une exécution de commandes à distance, la reconnaissance réseau, le vol de fichiers et l'effacement de logs pour dissimuler les traces.
*   **Attribution :** Suspicions portées sur un groupe APT sinophone, bien que les preuves soient jugées faibles (risque possible d'opération sous fausse bannière).
*   **Vulnérabilités :** Aucune CVE spécifique n'est associée, le vecteur reposant sur l'accès initial au système pour modifier les fichiers locaux de ViPNet.

**Recommandations :**
*   **Surveillance réseau :** Inspecter attentivement le trafic sortant sur les ports **5003** et **5060** (utilisés par HelloProxy) ainsi que le port **443** (utilisé par HelloBackdoor).
*   **Intégrité des fichiers :** Surveiller les modifications suspectes dans les répertoires d'installation des logiciels de sécurité.
*   **Analyse EDR :** Détecter l'injection de processus dans `svchost.exe` initiée par les composants de mise à jour de ViPNet.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-abuse-vipnet-software-to-target-russian-govt-agencies/){:target="_blank"}
