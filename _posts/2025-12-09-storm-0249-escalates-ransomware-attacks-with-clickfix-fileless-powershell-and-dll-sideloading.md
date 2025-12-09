---
title: 'Storm-0249 Escalates Ransomware Attacks with ClickFix, Fileless PowerShell, and DLL Sideloading'
date: 2025-12-09
permalink: /posts/2025/12/09/storm-0249-escalates-ransomware-attacks-with-clickfix-fileless-powershell-and-dll-sideloading/
tags:
- veille-cyber
- hackernews
---
**Storm-0249 : Évolution des Attaques de Ransomware**

Le groupe malveillant Storm-0249, précédemment connu pour son rôle d'intermédiaire dans l'accès initial, a fait évoluer ses tactiques en intégrant des méthodes plus sophistiquées pour mener des attaques de ransomware. Ces nouvelles approches visent à contourner les défenses, à s'établir de manière persistante et à opérer de façon indétectable.

**Points Clés et Vulnérabilités :**

*   **Changement de Tactique :** Abandon des campagnes de phishing de masse au profit d'attaques ciblées et précises.
*   **Utilisation de ClickFix :** Technique d'ingénierie sociale visant à inciter les victimes à exécuter des commandes malveillantes via la boîte de dialogue "Exécuter" de Windows, sous prétexte de résoudre un problème technique.
*   **Exécution de PowerShell Sans Fichier :** Exploitation de la commande légitime "curl.exe" pour télécharger et exécuter un script PowerShell malveillant à partir d'une URL trompeuse, se faisant passer pour un domaine Microsoft.
*   **DLL Sideloading :** Utilisation d'un package MSI malveillant pour installer une DLL infectée ("SentinelAgentCore.dll") aux côtés d'un exécutable légitime de la solution de sécurité SentinelOne ("SentinelAgentWorker.exe"). Lors du lancement de l'exécutable légitime, la DLL malveillante est chargée à son insu, permettant une exécution furtive.
*   **Utilisation d'Utilitaires Windows Légitimes :** Recours à des outils tels que `reg.exe` et `findstr.exe` pour collecter des identifiants système uniques (par exemple, MachineGuid). Ces données sont ensuite utilisées pour lier les clés de chiffrement aux systèmes des victimes, rendant le déchiffrement des données impossible sans la clé contrôlée par l'attaquant.
*   **Communication Chiffrée :** La DLL malveillante établit une communication chiffrée avec un serveur de commande et de contrôle (C2).

**Vulnérabilités Spécifiques (non détaillées avec des CVE dans l'article) :**

Bien que l'article ne mentionne pas de CVE spécifiques, les vulnérabilités exploitées sont liées à :

*   La confiance accordée aux processus signés et aux exécutables légitimes.
*   Les techniques d'ingénierie sociale (ClickFix).
*   L'exécution de scripts à distance via PowerShell.
*   La capacité des acteurs malveillants à se faire passer pour des entités de confiance.

**Recommandations :**

*   **Renforcement des Défenses :** Mettre en place des mesures de sécurité robustes pour détecter et bloquer les techniques avancées comme le DLL sideloading et l'exécution de scripts sans fichier.
*   **Sensibilisation des Utilisateurs :** Former les employés à reconnaître les tactiques d'ingénierie sociale, à se méfier des liens et des téléchargements inattendus, même s'ils semblent provenir de sources légitimes.
*   **Surveillance des Processus :** Monitorer attentivement l'exécution des processus, en particulier ceux qui chargent des DLL depuis des emplacements non standards ou qui présentent un comportement suspect.
*   **Gestion des Patchs :** Maintenir à jour tous les systèmes d'exploitation et logiciels, y compris les solutions de sécurité, pour corriger les vulnérabilités connues.
*   **Segmentation du Réseau :** Limiter la propagation latérale des menaces en segmentant le réseau.
*   **Authentification Forte :** Implémenter l'authentification multifacteur pour renforcer la sécurité des accès.

---
[Source](https://thehackernews.com/2025/12/storm-0249-escalates-ransomware-attacks.html){:target="_blank"}
