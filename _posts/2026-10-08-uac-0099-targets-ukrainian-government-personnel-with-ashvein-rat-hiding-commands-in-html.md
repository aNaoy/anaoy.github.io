---
title: 'UAC-0099 Targets Ukrainian Government Personnel With ASHVEIN RAT Hiding Commands in HTML'
date: 2026-10-08
permalink: /posts/2026/10/08/uac-0099-targets-ukrainian-government-personnel-with-ashvein-rat-hiding-commands-in-html/
tags:
- veille-cyber
- hackernews
---
### ASHVEIN : Nouvelle menace cybernétique contre le gouvernement ukrainien

Le groupe de menace aligné sur la Russie **UAC-0099** (également suivi sous le nom de **Earth Sirrush**) déploie un nouveau cheval de Troie d'accès à distance (RAT) baptisé **ASHVEIN** (ou *TelemetryBrowser*) pour espionner des entités gouvernementales, militaires et logistiques ukrainiennes. Ce groupe agit fréquemment comme courtier en accès initial pour le groupe APT **Sandworm**.

#### Points clés
*   **Techniques évolutives :** Le groupe a abandonné le PowerShell et Go au profit de binaires C# et .NET protégés, dissimulés via stéganographie.
*   **Dissimulation innovante :** ASHVEIN intègre ses commandes au sein d'éléments HTML invisibles.
*   **Vecteurs d'infection :** Utilisation de DLL sideloading (*FORGECLAMP*), de conteneurs VHD, et de droppers .NET piégés (ex: *AnswerFromPolice* imitant la police nationale ukrainienne).
*   **Tentative de manipulation d'IA :** Le groupe a expérimenté une technique nommée "GuardBreaker" insérant des requêtes malveillantes dans des scripts VBS pour saturer les mécanismes de sécurité des outils d'analyse basés sur l'IA.

#### Fonctionnalités d'ASHVEIN
*   Vol d'identifiants (Chrome, Firefox).
*   Capture d'écran et énumération de fichiers.
*   Exécution de commandes PowerShell à distance.
*   Fingerprinting système via WMI.
*   Communication C2 chiffrée avec mécanisme de secours basé sur GitHub.

#### Vulnérabilités et menaces associées
*   **Vulnérabilités :** L'article ne mentionne pas de CVE spécifique, mais souligne l'usage intensif de méthodes de chargement légitimes détournées comme le **DLL Sideloading**.
*   **Familles de malwares liés :** MATCHBOIL (loader), DRAGSTARE (stealer), LUNCHPOKE, et divers backdoors comme CINDERBLOT ou MeowMeow.

#### Recommandations
*   **Surveillance des processus :** Détecter les exécutions anormales de fichiers .NET et les comportements suspects liés au DLL Sideloading.
*   **Analyse des emails :** Sensibiliser le personnel aux leurres institutionnels (faux documents officiels, comme les réponses de la police).
*   **Protection des endpoints :** Mettre en place des solutions EDR capables d'analyser les comportements en temps réel plutôt que les signatures statiques, étant donné la mutation rapide des outils de l'attaquant.
*   **Filtrage réseau :** Surveiller les communications vers GitHub si elles ne sont pas nécessaires, en tant que mécanisme de "dead drop" pour le C2.

---
[Source](https://thehackernews.com/2026/10/uac-0099-targets-ukrainian-government.html){:target="_blank"}
