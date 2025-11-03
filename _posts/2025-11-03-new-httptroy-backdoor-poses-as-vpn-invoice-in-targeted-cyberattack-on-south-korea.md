---
title: 'New HttpTroy Backdoor Poses as VPN Invoice in Targeted Cyberattack on South Korea'
date: 2025-11-03
permalink: /posts/2025/11/03/new-httptroy-backdoor-poses-as-vpn-invoice-in-targeted-cyberattack-on-south-korea/
tags:
- veille-cyber
- hackernews
---
**HttpTroy : Une nouvelle porte dérobée sophistiquée ciblée sur la Corée du Sud**

Un groupe d'acteurs de menace lié à la Corée du Nord, connu sous le nom de Kimsuky, a déployé une porte dérobée inédite nommée HttpTroy dans le cadre d'une cyberattaque ciblée visant une seule entité en Corée du Sud. L'attaque a exploité une technique d'ingénierie sociale en se faisant passer pour une facture VPN afin de distribuer le logiciel malveillant.

**Points Clés :**

*   **Nature de la Menace :** HttpTroy est une porte dérobée sophistiquée capable de diverses actions malveillantes.
*   **Acteur de la Menace :** Kimsuky, un groupe d'acteurs de menace présumé lié à la Corée du Nord.
*   **Cible :** Une entité unique en Corée du Sud.
*   **Méthode d'Infection :** Une attaque de spear-phishing utilisant un fichier ZIP déguisé en facture VPN.
*   **Chaîne d'Infection :** L'attaque se déroule en trois étapes : un petit "dropper", un "loader" appelé MemLoad, et la porte dérobée finale, HttpTroy.
*   **Persistance :** MemLoad établit la persistance sur le système compromis en créant une tâche planifiée nommée "AhnlabUpdate", imitant ainsi la société de cybersécurité sud-coréenne AhnLab.
*   **Fonctionnalités de la Porte Dérobée :** HttpTroy offre un contrôle total sur le système compromis, permettant le transfert de fichiers, la capture d'écran, l'exécution de commandes arbitraires avec des privilèges élevés, le chargement d'exécutables en mémoire, l'établissement d'un "reverse shell", la terminaison de processus et la suppression de traces.
*   **Obfuscation :** Le malware utilise de multiples couches d'obfuscation, notamment des techniques de hachage personnalisées pour les appels d'API et des opérations XOR et SIMD pour les chaînes de caractères, rendant l'analyse et la détection difficiles. Les hachages et les chaînes d'API ne sont pas réutilisés et sont reconstruits dynamiquement.
*   **Communication C2 :** HttpTroy communique avec son serveur de commande et de contrôle (C2) via des requêtes HTTP POST vers `load.auraria[.]org`.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques exploitées. L'accès initial est supposé être un email de phishing, en l'absence de vulnérabilités de sécurité connues qui auraient pu être exploitées pour obtenir un premier accès.

**Recommandations :**

*   **Vigilance accrue face aux emails de phishing :** Les utilisateurs doivent faire preuve d'une extrême prudence avec les emails inattendus, en particulier ceux contenant des pièces jointes ou des liens.
*   **Inspection des pièces jointes suspectes :** Ne pas ouvrir les pièces jointes dont la provenance est douteuse ou dont le contenu semble inhabituel, comme des factures ou des documents inattendus.
*   **Mise à jour et surveillance des logiciels de sécurité :** Assurer la mise à jour régulière des solutions antivirus et anti-malware, et surveiller les alertes de sécurité.
*   **Renforcement des mesures de détection et de réponse :** Mettre en œuvre des stratégies de sécurité robustes pour détecter et répondre aux menaces sophistiquées.

---
[Source](https://thehackernews.com/2025/11/new-httptroy-backdoor-poses-as-vpn.html){:target="_blank"}
