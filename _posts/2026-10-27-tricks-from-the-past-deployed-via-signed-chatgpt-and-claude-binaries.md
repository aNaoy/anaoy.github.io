---
title: 'Tricks from the Past deployed via signed ChatGPT and Claude binaries'
date: 2026-10-27
permalink: /posts/2026/10/27/tricks-from-the-past-deployed-via-signed-chatgpt-and-claude-binaries/
tags:
- veille-cyber
- zerodaysfans
---
### Campagne de malwares Yoba : Abus des outils d'IA et DLL Sideloading

La campagne « Yoba » utilise des projets GitHub frauduleux imitant des applications de bureau basées sur des outils d'IA populaires (ChatGPT, Claude) pour distribuer des malwares. Les attaquants exploitent l'optimisation pour les moteurs de recherche (SEO poisoning) pour positionner leurs faux logiciels dans les résultats de recherche, incitant les utilisateurs à télécharger des archives ZIP contenant des exécutables légitimes signés par OpenAI ou Anthropic.

#### Points clés
*   **Technique d'infection :** Utilisation du **DLL sideloading**. Le malware remplace une DLL légitime par une version malveillante (ex: `winmm.dll`) chargée par l'exécutable légitime de l'application d'IA.
*   **Infrastructure furtive :** Pas de serveur de commande (C2) traditionnel. Les attaquants utilisent Telegram pour héberger des images contenant des données de configuration, le DNS-over-HTTPS (DoH) pour récupérer des ordres chiffrés et des services tiers comme Catbox pour le téléchargement des charges utiles finales.
*   **Persistance et évasion :** Utilisation de tâches planifiées usurpant l'identité de composants Windows, vérification des privilèges administrateur et mécanismes anti-sandbox/anti-analyse complexes.
*   **Payload final :** Dans les cas observés, le malware déploie le mineur de cryptomonnaie **XMRig** via le réseau Tor, mais la structure modulaire permet le déploiement de n'importe quel autre type de charge utile.

#### Vulnérabilités exploitées
*   **DLL Sideloading :** Exploitation de la manière dont les applications chargent leurs bibliothèques dépendantes sans vérification stricte du chemin d'accès.
*   **Absence de vérification des sources :** La confiance des utilisateurs envers des projets hébergés sur GitHub et bien référencés sur Google.
*   **Aucune CVE spécifique n'est mentionnée** dans le rapport, car il s'agit d'une technique d'abus de fonctionnalités légitimes plutôt que de l'exploitation d'une faille logicielle connue.

#### Recommandations
*   **Téléchargement sécurisé :** Téléchargez uniquement les logiciels depuis les sites officiels des éditeurs. Méfiez-vous des projets GitHub tiers proposant des versions « de bureau » non officielles d'outils en ligne.
*   **Vigilance administrative :** Ne jamais exécuter de programme avec des privilèges d'administrateur sans une nécessité absolue et une vérification de la source du fichier.
*   **Politique de sécurité :** Restreindre l'exécution de logiciels provenant de sources non approuvées via des stratégies de groupe (AppLocker ou Windows Defender Application Control).
*   **Surveillance réseau :** Surveiller les requêtes inhabituelles vers des services DNS-over-HTTPS (DoH) et le trafic sortant vers des nœuds Tor ou des plateformes de partage de fichiers temporaires (Catbox).
*   **Analyse comportementale :** Utiliser des solutions EDR capables de détecter le comportement de chargement de DLL suspectes ou les processus injectés (comme `svchost.exe` exécutant du minage).

---
[Source](https://research.checkpoint.com/2026/tricks-from-the-past-deployed-via-signed-chatgpt-and-claude-binaries/){:target="_blank"}
