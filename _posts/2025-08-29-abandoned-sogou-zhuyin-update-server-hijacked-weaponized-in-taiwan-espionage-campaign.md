---
title: 'Abandoned Sogou Zhuyin Update Server Hijacked, Weaponized in Taiwan Espionage Campaign'
date: 2025-08-29
permalink: /posts/2025/08/29/abandoned-sogou-zhuyin-update-server-hijacked-weaponized-in-taiwan-espionage-campaign/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage : Le serveur Sogou Zhuyin détourné

Une campagne d'espionnage, baptisée TAOTH, a ciblé des dissidents, journalistes, chercheurs et dirigeants dans plusieurs pays d'Asie de l'Est, dont Taïwan (49% des victimes), le Cambodge (11%) et les États-Unis (7%). Les attaquants ont détourné un serveur de mise à jour abandonné du logiciel d'édition Sogou Zhuyin pour distribuer plusieurs familles de logiciels malveillants, notamment C6DOOR, GTELAM, DESFY et TOSHIS.

Le processus d'infection débute par le téléchargement d'un installateur Sogou Zhuyin, qui semble inoffensif. Cependant, lors de la mise à jour automatique, le programme "ZhuyinUp.exe" récupère une configuration malveillante depuis un serveur compromis.

**Points Clés :**

*   **Détournement de serveur :** Un serveur de mise à jour de Sogou Zhuyin, non mis à jour depuis 2019, a été contrôlé par des acteurs malveillants en octobre 2024 pour distribuer des malwares.
*   **Ciblage géographique :** Principalement l'Asie de l'Est, avec Taïwan comme cible majeure.
*   **Profil des victimes :** Militants, journalistes, chercheurs, leaders technologiques et économiques.
*   **Chaînes d'infection sophistiquées :** Mises à jour logicielles détournées, fausses pages de connexion et de stockage cloud.
*   **Exfiltration de données via le cloud :** Utilisation de services comme Google Drive pour dissimuler le trafic et exfiltrer des informations.
*   **Utilisation de plusieurs familles de malwares :** C6DOOR, GTELAM, DESFY, TOSHIS.
*   **Attaques de spear-phishing :** Utilisation de fausses pages de connexion et de stockage cloud pour obtenir des consentements OAuth ou distribuer des malwares.

**Vulnérabilités et Malwares :**

*   **Vulnérabilité exploitée :** Le détournement d'un serveur de mise à jour de logiciel légitime, non sécurisé après abandon. L'article ne mentionne pas de CVE spécifiques associées à ces malwares ou à cette technique de détournement.
*   **TOSHIS :** Loader distribuant des charges utiles de second niveau (Cobalt Strike ou agent Merlin). Variante de Xiangoop, potentiellement liée au groupe Tropic Trooper.
*   **DESFY :** Logiciel espion collectant des noms de fichiers sur le Bureau et dans le répertoire des programmes.
*   **GTELAM :** Logiciel espion collectant des noms de fichiers avec des extensions spécifiques (PDF, DOC, DOCX, XLS, XLSX, PPT, PPTX) et les exfiltrant vers Google Drive.
*   **C6DOOR :** Backdoor personnalisée en Go, utilisant les protocoles HTTP et WebSocket pour le contrôle et la commande. Permet la collecte d'informations système, l'exécution de commandes, les opérations sur les fichiers, les captures d'écran, et l'injection de shellcode. Présence de caractères chinois simplifiés suggérant une origine chinoise.

**Recommandations :**

*   **Auditer régulièrement les environnements :** Identifier et remplacer les logiciels obsolètes ou sans support.
*   **Vérifier les permissions des applications cloud :** Examiner attentivement les autorisations demandées avant de les accorder.

---
[Source](https://thehackernews.com/2025/08/abandoned-sogou-zhuyin-update-server.html){:target="_blank"}
