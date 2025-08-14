---
title: 'Hackers Found Using CrossC2 to Expand Cobalt Strike Beacon’s Reach to Linux and macOS'
date: 2025-08-14
permalink: /posts/2025/08/14/hackers-found-using-crossc2-to-expand-cobalt-strike-beacons-reach-to-linux-and-macos/
tags:
- veille-cyber
- hackernews
---
## Extension de Cobalt Strike vers Linux et macOS

Des incidents récents ont révélé l'utilisation du framework de commande et contrôle (C2) CrossC2. Cet outil permet d'étendre les capacités de Cobalt Strike à des plateformes comme Linux et macOS, facilitant ainsi le contrôle inter-plateformes des systèmes. L'activité a été détectée entre septembre et décembre 2024, touchant plusieurs pays, dont le Japon.

Les attaquants ont utilisé CrossC2, ainsi que des outils tels que PsExec, Plink et Cobalt Strike, pour tenter de pénétrer les environnements Active Directory. Ils ont employé un chargeur personnalisé pour Cobalt Strike, baptisé ReadNimeLoader, qui utilise le langage de programmation Nim. ReadNimeLoader s'appuie sur OdinLdr, un chargeur de shellcode open-source, pour exécuter le module Cobalt Strike Beacon directement en mémoire, afin d'éviter toute trace sur disque. Des techniques anti-débogage et anti-analyse sont intégrées pour complexifier la détection.

Cette campagne d'attaques présente des similitudes avec des activités associées au ransomware BlackSuit/Black Basta, notamment dans l'utilisation de domaines C2 et de noms de fichiers similaires. La présence de versions ELF de SystemBC, un backdoor souvent utilisé comme précurseur au déploiement de Cobalt Strike et de ransomwares, a également été observée.

L'utilisation de CrossC2 pour compromettre des serveurs Linux au sein d'un réseau interne est particulièrement préoccupante, étant donné que de nombreux serveurs Linux ne disposent pas de systèmes de détection et de réponse (EDR) ou de systèmes similaires, ce qui en fait des points d'entrée potentiels pour des compromissions ultérieures.

### Points Clés :

*   **Outil principal :** CrossC2, permettant l'extension de Cobalt Strike à Linux et macOS.
*   **Techniques d'exécution :** Utilisation de ReadNimeLoader (écrit en Nim) et OdinLdr pour charger Cobalt Strike Beacon en mémoire.
*   **Méthode d'injection :** Sideloading de ReadNimeLoader ("jli.dll") via le binaire légitime `java.exe` lancé par une tâche planifiée.
*   **Fuite :** Évite les traces sur disque en exécutant le code en mémoire.
*   **Techniques d'évasion :** Intégration de méthodes anti-débogage et anti-analyse.
*   **Association :** Chevauchement potentiel avec les activités de BlackSuit/Black Basta.
*   **Outils associés :** PsExec, Plink, SystemBC (versions ELF observées).
*   **Cible :** Environnements Active Directory, avec une attention particulière aux serveurs Linux sous-protégés.

### Vulnérabilités :

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans cet article. L'accent est mis sur l'utilisation d'outils et de techniques par les attaquants pour exploiter l'infrastructure existante et les systèmes sous-protégés.

### Recommandations :

*   **Surveillance accrue :** Porter une attention particulière aux activités sur les serveurs Linux, qui sont souvent moins protégés par des solutions EDR.
*   **Sécurisation des serveurs :** Mettre en place des systèmes de détection et de réponse (EDR) ou des solutions de sécurité équivalentes sur les serveurs Linux.
*   **Analyse des artefacts :** Analyser les artefacts tels que les tâches planifiées, les binaires suspects (comme `java.exe` utilisé pour le sideloading) et les communications réseau inhabituelles.
*   **Veille sur les menaces :** Suivre les évolutions des outils et techniques utilisés par les acteurs malveillants, notamment ceux liés à Cobalt Strike et aux groupes comme BlackSuit/Black Basta.
*   **Chasse aux menaces :** Effectuer des recherches proactives pour identifier les signes d'infection par des chargeurs comme ReadNimeLoader et OdinLdr.

---
[Source](https://thehackernews.com/2025/08/researchers-warn-crossc2-expands-cobalt.html){:target="_blank"}
