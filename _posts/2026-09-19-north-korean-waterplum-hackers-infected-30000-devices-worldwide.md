---
title: 'North Korean WaterPlum hackers infected 30,000 devices worldwide'
date: 2026-09-19
permalink: /posts/2026/09/19/north-korean-waterplum-hackers-infected-30000-devices-worldwide/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'espionnage et de fraude financière du groupe nord-coréen WaterPlum

Le groupe de hackers nord-coréens WaterPlum a compromis plus de 30 000 appareils dans 100 pays entre décembre 2025 et juillet 2026. Lié aux services de renseignement militaire nord-coréens, ce groupe finance les programmes d'armement du régime via le vol de cryptomonnaies (plus de 10,7 millions USD détournés) et l'espionnage industriel.

**Points clés :**
*   **Mode opératoire :** Ciblage de développeurs et de chercheurs d'emploi via de fausses offres sur des plateformes de recrutement ou des réseaux sociaux. L'usage de deepfakes (échange de visages) lors d'entretiens vidéo est fréquent pour masquer l'identité des attaquants.
*   **Double menace :** Certains hackers agissent en tant qu'employés informatiques distants pour infiltrer des entreprises, tout en utilisant des identités volées pour obtenir d'autres postes.
*   **Objectifs :** Vol d'identifiants, de clés privées de portefeuilles crypto, de données sensibles, et pivot vers les réseaux des entreprises clientes ou employeurs.

**Malwares identifiés :**
*   **BeaverTail :** Malware JavaScript dissimulé dans des paquets npm.
*   **InvisibleFerret :** Backdoor basée sur Python.
*   **OtterCookie & OtterCandy :** Chevaux de Troie d'accès à distance (RAT) et voleurs d'informations (info-stealers).
*   **StoatWaffle :** Malware modulaire Node.js utilisant des configurations malveillantes dans des projets Visual Studio Code.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifique, car les attaques reposent sur l'ingénierie sociale (téléchargement volontaire de projets malveillants, exécution de code lors de tests techniques) plutôt que sur l'exploitation directe de failles logicielles non corrigées.

**Recommandations :**
*   **Vérification rigoureuse :** Confirmer systématiquement l'identité, la localisation et les qualifications des candidats lors des recrutements distants.
*   **Sandboxing :** Ne jamais exécuter de code ou de projets inconnus en dehors d'environnements isolés (sandbox).
*   **Inspection de code :** Analyser les fichiers fournis (notamment les dossiers VS Code) pour détecter toute commande suspecte téléchargeant des payloads externes.
*   **Principe du moindre privilège :** Restreindre strictement l'accès des collaborateurs (surtout distants) aux seuls systèmes et données nécessaires à l'accomplissement de leur mission.

---
[Source](https://www.bleepingcomputer.com/news/security/north-korean-waterplum-hackers-infected-30-000-devices-worldwide/){:target="_blank"}
