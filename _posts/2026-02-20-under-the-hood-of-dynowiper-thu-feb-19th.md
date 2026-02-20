---
title: 'Under the Hood of DynoWiper, (Thu, Feb 19th)'
date: 2026-02-20
permalink: /posts/2026/02/20/under-the-hood-of-dynowiper-thu-feb-19th/
tags:
- veille-cyber
- sans-isc
---
**Analyse de DynoWiper : un destructeur de données ciblant les entreprises d'énergie**

Ce rapport détaille le fonctionnement de DynoWiper, un logiciel malveillant de type "wiper" utilisé lors d'attaques contre des entreprises d'énergie polonaises fin décembre 2025. L'analyse technique pointe vers des acteurs étatiques russes, potentiellement liés au groupe APT Sandworm, connu pour ses actions passées contre des infrastructures critiques.

**Points Clés :**

*   **Fonctionnement :** DynoWiper corrompt les données en écrivant des blocs de données aléatoires à des endroits spécifiques des fichiers et supprime ensuite ces fichiers.
*   **Initialisation :** Le malware initialise un générateur de nombres pseudo-aléatoires Mersenne Twister (MT19937) avec une valeur de départ fixe, puis le réinitialise avec une valeur aléatoire.
*   **Corruption des données :** Le logiciel parcourt récursivement les lecteurs logiques (fixes et amovibles), identifie les fichiers cibles (en excluant certains répertoires système critiques comme `system32`, `windows`, `program files`) et modifie leurs attributs. Pour chaque fichier, il écrit 16 octets de données aléatoires au début, puis, si le fichier est plus grand, il écrit à des emplacements pseudo-aléatoires jusqu'à 4096 fois.
*   **Suppression des données :** Après la corruption, DynoWiper supprime directement les fichiers ciblés.
*   **Finalisation :** Le malware obtient son propre jeton de processus, active le privilège `SeShutdownPrivilege` et déclenche un redémarrage du système pour masquer ses traces et potentiellement perturber davantage l'environnement.
*   **Liens MITRE ATT&CK :** L'activité de DynoWiper correspond à plusieurs tactiques et techniques, notamment la découverte locale (T1680, T1083), l'évasion de défense via la modification des permissions de fichiers (T1222) et la manipulation des jetons d'accès (T1134), l'escalade de privilèges (T1134) et l'impact par la destruction de données (T1485) et l'arrêt du système (T1529).

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article concernant DynoWiper lui-même. Le logiciel exploite les fonctionnalités légitimes du système d'exploitation pour atteindre ses objectifs destructeurs.

**Recommandations :**

Bien que l'article se concentre sur l'analyse technique, les informations fournies impliquent des recommandations générales pour la sécurité :

*   **Détection et réponse :** Mettre en place des mécanismes de détection robustes pour identifier les comportements suspects tels que la corruption de fichiers à grande échelle et les modifications de privilèges de processus.
*   **Sauvegardes :** Maintenir des sauvegardes régulières et testées hors ligne des données critiques.
*   **Gestion des accès :** Appliquer le principe du moindre privilège pour limiter les dommages potentiels en cas d'infection.
*   **Surveillance :** Surveiller activement les journaux système et réseau pour détecter toute activité inhabituelle.
*   **Intelligence sur les menaces :** Se tenir informé des dernières menaces et des tactiques utilisées par les groupes d'attaquants connus.

---
[Source](https://isc.sans.edu/diary/rss/32730){:target="_blank"}
