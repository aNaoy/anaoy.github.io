---
title: 'HollowFrame Loader Deploys Matryoshka Backdoor in Spear-Phishing Attack on Law Firm'
date: 2026-07-31
permalink: /posts/2026/07/31/hollowframe-loader-deploys-matryoshka-backdoor-in-spear-phishing-attack-on-law-firm/
tags:
- veille-cyber
- hackernews
---
### Analyse de la campagne d'attaques HollowFrame et Matryoshka

Des chercheurs en cybersécurité ont identifié une nouvelle campagne de spear-phishing visant un cabinet d'avocats, utilisant un framework de chargement en Go baptisé **HollowFrame** pour déployer une famille de backdoors en Rust nommée **Matryoshka**.

**Points clés :**
*   **Vecteur d'attaque :** Un email de phishing contenant un lien vers une archive chiffrée, laquelle héberge un raccourci Windows (LNK) masqué en « documents de dossier ».
*   **Méthodologie :** L'attaque utilise le chargement latéral de DLL (*DLL side-loading*) avec des fichiers légitimes (ex: `python.exe`) pour exécuter des composants malveillants.
*   **Techniques d'évasion :** Le malware intègre des contrôles anti-analyse (vérification de la mémoire, des mouvements de souris et du temps de fonctionnement système) et utilise des tâches planifiées pour maintenir sa persistance.
*   **Infrastructure C2 :** Matryoshka se décline en deux versions : l'une communiquant via HTTP et l'autre détournant des dépôts GitHub privés pour gérer les commandes et exfiltrer les données de chaque victime de manière segmentée.

**Vulnérabilités exploitées :**
*   Bien qu'aucune CVE spécifique ne soit mentionnée, l'attaque exploite le **DLL side-loading**, une faiblesse liée à la manière dont Windows recherche les bibliothèques nécessaires à l'exécution d'un programme, permettant d'exécuter du code arbitraire en plaçant une DLL malveillante dans le répertoire de l'application.

**Recommandations :**
*   **Formation des utilisateurs :** Sensibiliser le personnel à la méfiance vis-à-vis des liens dans les emails et des fichiers archivés non sollicités.
*   **Durcissement de la configuration :** Surveiller les comportements anormaux des processus système (ex: `python.exe` lançant des tâches inattendues) et limiter l'exécution de scripts PowerShell via des politiques de groupe (GPO).
*   **Filtrage réseau :** Bloquer les connexions vers les domaines GitHub suspects identifiés dans les communications C2 et surveiller le trafic sortant vers des adresses IP inconnues.
*   **Protection des endpoints :** Utiliser des solutions EDR capables de détecter les techniques de persistance (tâches planifiées) et le chargement latéral de DLL.

---
[Source](https://thehackernews.com/2026/07/hollowframe-loader-deploys-matryoshka.html){:target="_blank"}
