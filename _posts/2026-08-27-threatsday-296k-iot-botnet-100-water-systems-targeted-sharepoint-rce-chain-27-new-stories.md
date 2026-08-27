---
title: 'ThreatsDay: 296K IoT Botnet, 100+ Water Systems Targeted, SharePoint RCE Chain + 27 New Stories'
date: 2026-08-27
permalink: /posts/2026/08/27/threatsday-296k-iot-botnet-100-water-systems-targeted-sharepoint-rce-chain-27-new-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces informatiques : automatisation, IA et vecteurs persistants

Le paysage cyber actuel est marqué par une réduction drastique des délais entre la divulgation d'une faille et son exploitation. Les attaquants exploitent des infrastructures décentralisées (blockchain) et l'IA pour accroître leur efficacité.

#### Points clés
*   **Diversification des C2 :** Utilisation de la blockchain Polygon (botnet *Aeternum*) et de bases de données cloud (framework *Miraak*) pour masquer les communications de commande et contrôle.
*   **Intégration de l'IA :** Le botnet *ToxNetV2* utilise l'IA pour décider des actions sur les hôtes infectés, tandis que des serveurs MCP (Model Context Protocol) malveillants visent à exfiltrer des secrets via des agents IA.
*   **Infrastructures critiques :** Plus de 100 systèmes de gestion des eaux aux États-Unis ont été ciblés via des automates (PLC) exposés sur Internet.
*   **Phishing en temps réel :** Le framework *JWR* permet un pilotage humain direct des sessions de phishing, allant au-delà de la simple capture de mots de passe pour voler des données biométriques et des sessions.
*   **Évasion complexe :** Multiplication des malwares utilisant des scores de suspicion pour détecter les environnements de sandbox (*ScarfaceStealer*).

#### Vulnérabilités critiques
*   **Microsoft SharePoint :** Chaîne d'exploitation combinant **CVE-2026-55040** (contournement d'authentification JWT) et **CVE-2026-63520** (exécution de code à distance).
*   **HP ThinPro :** Faille "Zero-day" dans le processus de démarrage permettant de contourner le chiffrement de disque TPM (via une mesure incomplète de la chaîne de boot).

#### Recommandations
*   **Renforcement du périmètre :** Réduire l'exposition directe des dispositifs industriels (PLC/Modems) sur Internet. Utiliser des accès distants sécurisés uniquement lorsque nécessaire.
*   **Gestion des correctifs :** Accélérer les cycles de patch, particulièrement pour les serveurs SharePoint. En l'absence de correctif immédiat, instaurer une défense périmétrique réseau ("control plane") pour limiter l'exploitabilité.
*   **Sécurisation des terminaux :** Activer le *Secure Boot* et configurer des mots de passe BIOS sur les équipements de type client léger (HP ThinPro).
*   **Gouvernance de l'IA :** Mettre en place une supervision IT sur les outils IA et serveurs MCP utilisés en entreprise, car 80 % d'entre eux échappent actuellement au contrôle, favorisant l'exfiltration de données via des accès légitimes.
*   **Sensibilisation :** Se méfier des sites de "scan de sécurité" incitant à désinstaller les solutions antivirus existantes ou des applications de productivité (PDF/Conversion) non vérifiées.

---
[Source](https://thehackernews.com/2026/08/threatsday-296k-iot-botnet-100-water.html){:target="_blank"}
