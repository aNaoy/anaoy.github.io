---
title: 'DarkBlinders Compromises Israeli Target and Iraqi Kurdish Government Cloud Environment'
date: 2026-11-02
permalink: /posts/2026/11/02/darkblinders-compromises-israeli-target-and-iraqi-kurdish-government-cloud-environment/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage cybernétique : DarkBlinders cible Israël et l'Irak

Le groupe de menace **DarkBlinders** (lié à l'Iran) mène une campagne d'espionnage active depuis septembre 2024, visant principalement des infrastructures gouvernementales et des individus à haut profil en Israël et au Kurdistan irakien. Ce groupe est étroitement lié aux opérations des clusters UNC5795 et potentiellement au groupe APT34.

**Points clés :**
*   **Tactiques d'accès initial :** Utilisation intensive de l'ingénierie sociale (fausses offres d'emploi, usurpation d'identités comme l'IT de l'aéroport de Dubaï) et de phishing.
*   **Outils malveillants :** Utilisation de la suite **SHELBYLOADER** (V2) et **SHELBYC2** (ou AEROSTAT). Le groupe déploie également l'utilitaire de tunnelisation **Blackwood** et une fausse application de visioconférence nommée "StarkMeet".
*   **Infrastructure :** Utilisation de GitHub pour le C2 (Command & Control) et de domaines imitant des services légitimes (Outlook, Microsoft OneDrive, portails gouvernementaux).

**Vulnérabilités et techniques exploitées :**
*   **AppDomainManager Injection :** Technique utilisée pour charger des bibliothèques malveillantes via des fichiers `.csproj`.
*   **DLL Sideloading :** Exploitation du chargement de DLL légitimes pour injecter des composants malveillants.
*   **Contournement des logs :** Manipulation des événements de suivi Windows (ETW - Event Tracing for Windows) pour masquer l'exécution.
*   *Note : Aucune CVE spécifique n'est mentionnée, les attaques reposent sur l'exploitation de fonctionnalités de développement légitimes plutôt que sur des failles logicielles documentées.*

**Recommandations :**
*   **Sensibilisation :** Former le personnel à la vigilance face aux sollicitations professionnelles inattendues et aux tests de codage suspects (particulièrement ceux transmis via des projets Visual Studio).
*   **Durcissement des terminaux :** Restreindre l'exécution de projets C# non signés et surveiller l'injection `AppDomainManager` dans les processus critiques.
*   **Filtrage réseau :** Bloquer les domaines suspects identifiés (ex: `gcc-sg[.]cloud`, `stark-meet[.]com`) et surveiller les communications inhabituelles vers GitHub émanant de serveurs internes.
*   **Analyse comportementale :** Privilégier la détection basée sur le comportement des processus (sideloading de DLL, appels ETW suspects) plutôt que sur les signatures de fichiers statiques.

---
[Source](https://thehackernews.com/2026/11/darkblinders-compromises-israeli-target.html){:target="_blank"}
