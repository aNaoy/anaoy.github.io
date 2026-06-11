---
title: 'ThreatsDay Bulletin: Worm Code Leaked, AI Agent Phished, Claude Code Patch + 28 New Stories'
date: 2026-06-11
permalink: /posts/2026/06/11/threatsday-bulletin-worm-code-leaked-ai-agent-phished-claude-code-patch-28-new-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces et failles de sécurité (Juin 2026)

Le paysage actuel des menaces se caractérise par une professionnalisation accrue des attaques (Malware-as-a-Service), l'exploitation de la confiance accordée aux outils légitimes et la compromission des agents IA. Les attaquants délaissent souvent les exploits complexes au profit de techniques d'ingénierie sociale sophistiquées et de détournements de configurations.

#### Points clés
*   **Expansion du MaaS :** Les réseaux de blanchiment d'argent (Mule-as-a-Service) et les RAT (Remote Access Trojans) comme *SilabRAT* (5 000 $/mois) utilisent des techniques avancées comme le clonage de profil de navigateur pour contourner les protections.
*   **Infiltration de la supply chain :** Le framework *Miasma* a exposé plus de 300 composants sur des registres (npm, PyPI), transformant des outils de développement en vecteurs d'attaque. Des techniques de « download pumping » gonflent artificiellement la popularité de paquets malveillants.
*   **Agents IA sous surveillance :** Les agents IA (ex: Claude Code) sont ciblés par du « phishing d'agent » où des requêtes malveillantes incitent l'IA à exfiltrer des secrets CI/CD ou des identifiants cloud.
*   **Espionnage et ciblage étatique :** Le groupe nord-coréen *Famous Chollima* domine les intrusions manuelles, tandis que des acteurs liés à la Chine et à l'Iran multiplient les leurres (faux emplois, portails de recrutement) pour cibler des données sensibles.
*   **Neutralisation des EDR :** L'émergence de techniques comme *EDRChoker* (étranglement de bande passante via QoS) ou *EDRStartupHinder* permet de paralyser les outils de défense sans déclencher d'alertes de malware.

#### Vulnérabilités notables
*   **CVE-2026-49494 :** Vulnérabilité d'underflow entier dans le pilote de pare-feu Comodo (*Inspect.sys*). Permet de faire crasher un système à distance avec un seul paquet TCP/IP (Score CVSS : 7.5).
*   **Ghost-Sender :** Faille de configuration dans Microsoft Exchange permettant d'usurper n'importe quel expéditeur interne ou externe, contournant les politiques SPF, DKIM et DMARC.
*   **Claude Code (GitHub Action) :** Exposition de secrets CI/CD via un sandboxing insuffisant de l'outil « Read » (corrigé en v.2.1.128).

#### Recommandations
1.  **Auditer les accès des agents IA :** Restreindre strictement les permissions des agents et outils d'IA dans les pipelines CI/CD. Appliquer un principe de moindre privilège aux jetons d'accès (PAT).
2.  **Surveillance des configurations :** Auditer les politiques de QoS et les ACL système pour détecter toute tentative de bridage des outils de sécurité (EDR/AV).
3.  **Vigilance sur les dépendances :** Mettre en place une analyse stricte des paquets open-source (npm, PyPI) et ne pas se fier uniquement aux statistiques de téléchargement.
4.  **Gestion des identités :** Adopter une approche « zero-trust » en supposant que tout élément interne à la chaîne logicielle ou à l'infrastructure peut être compromis.
5.  **Hygiène des extensions :** Vérifier régulièrement les permissions des extensions de navigateur, en particulier celles interagissant avec des outils d'IA.

---
[Source](https://thehackernews.com/2026/06/threatsday-bulletin-worm-code-leaked-ai.html){:target="_blank"}
