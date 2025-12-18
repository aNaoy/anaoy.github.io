---
title: 'I am not a robot: ClickFix used to deploy StealC and Qilin'
date: 2025-12-18
permalink: /posts/2025/12/18/i-am-not-a-robot-clickfix-used-to-deploy-stealc-and-qilin/
tags:
- veille-cyber
- sophos
---
**ClickFix : un piège à visiteurs pour installer des malwares**

Une technique appelée "ClickFix" est utilisée par des acteurs malveillants pour installer des logiciels malveillants, tels que des voleurs d'informations (infostealers) et des ransomwares, sur les appareils des victimes. Cette méthode repose sur des requêtes de vérification humaine trompeuses qui incitent les utilisateurs à télécharger des malwares.

Les chercheurs ont observé une campagne où cette technique a été utilisée pour déployer le ransomware Qilin. L'infection initiale se produit lorsqu'un utilisateur visite un site web légitime mais compromis, où un script malveillant lance une série d'actions. Ces actions aboutissent à l'installation de NetSupport Manager, un outil d'accès à distance légitime souvent exploité par les cybercriminels (désigné comme NetSupport RAT).

Après l'installation de NetSupport RAT, un voleur d'informations appelé StealC V2 est téléchargé. Environ un mois plus tard, des notes de rançonciation du groupe Qilin apparaissent, indiquant que les attaquants ont accédé au réseau via des identifiants volés, potentiellement obtenus grâce à StealC. L'accès au réseau a été facilité par des identifiants compromis sur un appareil VPN Fortinet.

**Points clés :**

*   **Tendance :** "ClickFix" est une technique en évolution constante pour distribuer des malwares.
*   **Mécanisme :** Elle utilise de faux processus de vérification pour tromper les utilisateurs et les pousser à télécharger des malwares.
*   **Outils utilisés :** NetSupport Manager (exploité comme RAT) et StealC V2 (voleur d'informations) sont des composantes clés de la chaîne d'infection.
*   **Objectif final :** Le déploiement de ransomwares comme Qilin, utilisant une stratégie de double extorsion (chiffrement et exfiltration de données).

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est directement mentionnée dans l'article comme étant exploitée. L'attaque repose plutôt sur des tactiques d'ingénierie sociale et l'utilisation d'outils légitimes détournés.

**Recommandations :**

*   **Hygiène de cybersécurité :** Mettre en œuvre de bonnes pratiques de cybersécurité, incluant la gestion des correctifs (patch management) pour les appareils exposés sur Internet.
*   **Exposition des services :** Limiter l'exposition des services potentiellement vulnérables (comme le RDP) sur Internet uniquement lorsque cela est nécessaire.
*   **Authentification multifacteur (MFA) :** Implémenter une MFA robuste et résistante au phishing sur l'ensemble du réseau.
*   **Détection et réponse sur les points d'extrémité (EDR) :** Utiliser des solutions EDR pour identifier et atténuer les activités précurseurs des ransomwares.

---
[Source](https://news.sophos.com/en-us/2025/12/18/i-am-not-a-robot-clickfix-used-to-deploy-stealc-and-qilin/){:target="_blank"}
