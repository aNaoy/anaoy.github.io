---
title: 'Researchers Spot XZ Utils Backdoor in Dozens of Docker Hub Images, Fueling Supply Chain Risks'
date: 2025-08-12
permalink: /posts/2025/08/12/researchers-spot-xz-utils-backdoor-in-dozens-of-docker-hub-images-fueling-supply-chain-risks/
tags:
- veille-cyber
- hackernews
---
**Risques persistants : la faille XZ Utils toujours présente dans des images Docker**

De nouvelles recherches ont révélé la présence de la porte dérobée XZ Utils dans plusieurs images Docker sur Docker Hub, plus d'un an après la découverte initiale de l'incident. Ce problème souligne les risques pour la chaîne d'approvisionnement logicielle, car des images infectées ont servi de base à d'autres, propageant ainsi la menace de manière transitive.

**Points clés :**

*   La porte dérobée XZ Utils a été découverte dans 35 images Docker.
*   Des images construites sur ces bases infectées ont également été trouvées, amplifiant le risque.
*   La compromission a affecté les versions 5.6.0 et 5.6.1 de XZ Utils.
*   Le code malveillant, intégré dans la bibliothèque `liblzma.so` utilisée par le serveur OpenSSH, permettait un accès à distance non autorisé et l'exécution de charges utiles arbitraires.
*   L'attaque, attribuée à un développeur nommé "Jia Tan", a fait preuve d'une planification sophistiquée sur près de deux ans.
*   Malgré les efforts de correction, des images Debian infectées par la porte dérobée sont restées disponibles, présentées par les mainteneurs comme une "curiosité historique".
*   La persistance de ces artefacts dans l'écosystème des conteneurs, même après les correctifs, met en évidence la nécessité d'une surveillance continue au niveau binaire.

**Vulnérabilités :**

*   **CVE-2024-3094** (CVSS score : 10.0) : Décrit l'intégration d'une porte dérobée dans les versions 5.6.0 et 5.6.1 de XZ Utils.

**Recommandations :**

*   Mettre en œuvre une surveillance continue au niveau binaire pour détecter les logiciels malveillants dans les artefacts logiciels, au-delà du simple suivi des versions.
*   Être vigilant quant à l'utilisation d'images de conteneurs provenant de sources publiques et vérifier leur intégrité.
*   Analyser attentivement les dépendances et les chaînes d'approvisionnement logicielles pour identifier et atténuer les risques de propagation de vulnérabilités.

---
[Source](https://thehackernews.com/2025/08/researchers-spot-xz-utils-backdoor-in.html){:target="_blank"}
