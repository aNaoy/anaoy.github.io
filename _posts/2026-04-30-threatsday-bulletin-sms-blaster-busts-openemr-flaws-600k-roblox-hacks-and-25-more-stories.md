---
title: 'ThreatsDay Bulletin: SMS Blaster Busts, OpenEMR Flaws, 600K Roblox Hacks and 25 More Stories'
date: 2026-04-30
permalink: /posts/2026/04/30/threatsday-bulletin-sms-blaster-busts-openemr-flaws-600k-roblox-hacks-and-25-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces cyber : Attaques sur la chaîne d'approvisionnement et vulnérabilités critiques

Le paysage actuel de la cybersécurité est marqué par une intensification des attaques sur la chaîne d'approvisionnement logicielle (npm, PyPI, GitHub), l'exploitation de failles dans des outils légitimes (Komari) et une recrudescence des campagnes de phishing sophistiquées utilisant des technologies émergentes (SMS Blasters, kits AitM).

#### Points clés
*   **Chaîne d'approvisionnement :** Multiplication des empoisonnements de bibliothèques npm et PyPI visant à dérober des jetons d'accès et des portefeuilles crypto.
*   **Phishing nouvelle génération :** Utilisation de "SMS Blasters" (fausses antennes relais) et de kits de phishing avancés (Saiga 2FA) contournant les mesures de sécurité classiques.
*   **Exposition massive :** Plus de 3 millions de serveurs RDP/VNC sont exposés en ligne, souvent sans authentification ou avec des versions obsolètes.
*   **Vol de données :** Le malware *Vidar Stealer* domine le marché des voleurs d'informations, tandis que des extensions de navigateur vendent légalement les données de navigation.
*   **Fraude et influence :** Hausse exponentielle des arnaques sur les réseaux sociaux et campagnes d'influence persistantes (ex: Spamouflage).

#### Vulnérabilités majeures
*   **OpenEMR :** 38 vulnérabilités critiques dont **CVE-2026-24908** et **CVE-2026-23627** (Injections SQL, XSS, exécution de code).
*   **Qinglong :** Exploitation de **CVE-2026-3965** et **CVE-2026-4047** pour le déploiement de mineurs de cryptomonnaie.
*   **Windows :** Risque lié à **CVE-2019-0708 (BlueKeep)** toujours présent sur 19 000 serveurs, et faille locale **PhantomRPC** non corrigée par Microsoft.
*   **WordPress :** Backdoor découverte dans le plugin *Quick Page/Post Redirect*.

#### Recommandations
*   **Hygiène des accès :** Sécuriser les accès distants (RDP/VNC) par VPN, supprimer les versions obsolètes et activer l'authentification forte (MFA).
*   **Gestion des dépendances :** Auditer systématiquement les paquets open-source importés (npm, PyPI) et vérifier l'intégrité des workflows GitHub Actions.
*   **Veille et correctifs :** Appliquer les patchs de sécurité sans délai, particulièrement pour les plateformes critiques comme OpenEMR ou les outils de gestion de tâches.
*   **Sensibilisation :** Se méfier des messages inattendus, même s'ils semblent provenir de sources fiables (phénomène des SMS Blasters), et examiner les politiques de confidentialité des extensions de navigateur.
*   **Nettoyage de données :** Utiliser des outils (comme ALC-NG) pour purger les métadonnées et fichiers sensibles des documents destinés à être publiés en ligne (ex: publications scientifiques).

---
[Source](https://thehackernews.com/2026/04/threatsday-bulletin-sms-blaster-busts.html){:target="_blank"}
