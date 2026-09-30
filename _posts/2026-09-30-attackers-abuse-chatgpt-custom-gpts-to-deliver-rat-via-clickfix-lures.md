---
title: 'Attackers Abuse ChatGPT Custom GPTs to Deliver RAT via ClickFix Lures'
date: 2026-09-30
permalink: /posts/2026/09/30/attackers-abuse-chatgpt-custom-gpts-to-deliver-rat-via-clickfix-lures/
tags:
- veille-cyber
- hackernews
---
### Détournement de GPT personnalisés pour la distribution de RAT via ClickFix

Des attaquants exploitent la fonctionnalité « Custom GPT » de ChatGPT pour diffuser des logiciels malveillants de type RAT (Remote Access Trojan). En se faisant passer pour des services légitimes, ces agents conversationnels manipulent les utilisateurs pour les rediriger vers des sites malveillants utilisant la technique « ClickFix ».

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de publicités Google trompeuses menant à des GPT personnalisés malveillants.
*   **Ingénierie sociale :** Le GPT incite la victime à visiter un domaine Google Sites sous prétexte d'une erreur de disponibilité, où un faux CAPTCHA Cloudflare est présenté.
*   **Mécanisme ClickFix :** Le faux CAPTCHA pousse l'utilisateur à copier et exécuter manuellement une commande PowerShell malveillante.
*   **Chaîne d'infection :** La commande télécharge un installateur MSI qui procède à un *DLL sideloading* (via un binaire Canon légitime) pour injecter une charge utile cachée dans un fichier audio (.WAV).
*   **Capacités du RAT :** Le logiciel espion peut capturer l'écran, le son, les entrées clavier, voler des données de navigateurs et exécuter des scripts à distance. Il utilise DNS-over-HTTPS pour masquer ses communications avec le serveur de commande (C2).

**Vulnérabilités exploitées :**
Il ne s'agit pas de vulnérabilités logicielles classiques (CVE), mais de l'exploitation de la confiance accordée aux plateformes connues (ChatGPT, Google Sites) et de la manipulation de l'utilisateur final (ingénierie sociale). Le processus repose sur le détournement de fonctionnalités natives Windows (MSI, PowerShell, DLL sideloading) pour contourner les défenses.

**Recommandations :**
*   **Méfiance accrue :** Ne jamais exécuter de commandes PowerShell ou installer de fichiers (MSI, EXE) provenant de sites web, même s'ils semblent être des outils de vérification (CAPTCHA).
*   **Vérification des sources :** Accéder aux services en ligne directement par leur adresse officielle et non via des liens fournis par des agents conversationnels ou des résultats publicitaires.
*   **Sécurité des terminaux :** Maintenir les logiciels de sécurité à jour pour détecter les comportements suspects (comme le *DLL sideloading* ou l'accès non autorisé au micro/caméra).
*   **Sensibilisation :** Éduquer les utilisateurs sur les techniques de « ClickFix », où l'attaquant incite la victime à effectuer elle-même l'action malveillante (copier/coller une commande).

---
[Source](https://thehackernews.com/2026/09/attackers-abuse-chatgpt-custom-gpts-to.html){:target="_blank"}
