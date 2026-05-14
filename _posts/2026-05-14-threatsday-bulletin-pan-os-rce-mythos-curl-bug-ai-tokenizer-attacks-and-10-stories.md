---
title: 'ThreatsDay Bulletin: PAN-OS RCE, Mythos cURL Bug, AI Tokenizer Attacks, and 10+ Stories'
date: 2026-05-14
permalink: /posts/2026/05/14/threatsday-bulletin-pan-os-rce-mythos-curl-bug-ai-tokenizer-attacks-and-10-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces : Vulnérabilités critiques et évolutions des attaques

Le paysage de la cybersécurité est marqué par une recrudescence d'attaques exploitant des outils légitimes, des services cloud et des techniques d'ingénierie sociale sophistiquées. Les attaquants délaissent de plus en plus les malwares complexes au profit de détournements de workflows, de supply chain attacks et de manipulations de modèles d'IA.

#### Points clés
*   **Détournement d'IA :** Une technique de « tokenizer tampering » permet de prendre le contrôle des sorties de modèles IA sans modifier leurs poids, simplement en altérant le fichier `tokenizer.json`.
*   **Supply Chain :** Le groupe *TeamPCP* a lancé un « concours » de compromission de chaînes d'approvisionnement logicielles, utilisant un ver open-source pour inciter au piratage massif contre récompense financière.
*   **Techniques de verrouillage :** L'outil *GhostLock* illustre comment un utilisateur disposant de droits de lecture peut bloquer l'accès à des fichiers partagés (via `CreateFileW`), produisant un impact similaire à un ransomware sans chiffrement.
*   **C2 innovants :** Des attaquants utilisent désormais le système de messagerie haute performance *NATS* comme canal de communication pour leurs serveurs de commande et contrôle (C2), compliquant la détection traditionnelle.
*   **Campagnes ciblées :** Plusieurs campagnes de phishing utilisent des thématiques liées à l'aide humanitaire ou à de faux supports informatiques (ex: Microsoft Teams) pour déployer des RAT (Remote Access Trojans) et exfiltrer des données.

#### Vulnérabilités notables
*   **CVE-2026-0300 :** Vulnérabilité critique de dépassement de tampon dans le service d'authentification User-ID de PAN-OS (Palo Alto Networks), permettant l'exécution de code arbitraire avec des privilèges root.
*   **CVE-2026-33017 :** faille RCE non authentifiée dans *Langflow*, exploitée pour déployer des infrastructures C2.
*   **CVE-2023-36036 :** Utilisée pour l'élévation de privilèges au niveau SYSTEM dans le cadre de campagnes d'usurpation de support informatique.

#### Recommandations
*   **Appliquer les correctifs :** La priorité absolue est la mise à jour immédiate des équipements Palo Alto Networks pour contrer l'exploitation active de la CVE-2026-0300.
*   **Durcir les accès :** Renforcer les contrôles d'autorisation sur les API et les partages de fichiers SMB pour prévenir les fuites de données (« zero-auth ») et les techniques de blocage type *GhostLock*.
*   **Vigilance sur les outils :** Surveiller étroitement l'utilisation d'outils d'administration légitimes (ScreenConnect, PowerShell, Python) et des infrastructures de communication cloud (NATS, GitHub Releases) souvent détournés pour des activités malveillantes.
*   **Sécuriser les déploiements IA :** Valider l'intégrité des fichiers de configuration (notamment `tokenizer.json`) lors de l'intégration de modèles IA tiers dans les environnements de production.
*   **Sensibilisation :** Maintenir une méfiance active vis-à-vis des messages de support technique non sollicités et des offres de logiciels « gratuits » provenant de forums ou de sources non vérifiées.

---
[Source](https://thehackernews.com/2026/05/threatsday-bulletin-pan-os-rce-mythos.html){:target="_blank"}
