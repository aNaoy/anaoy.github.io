---
title: 'Researchers Detail Tuoni C2s Role in an Attempted 2025 Real-Estate Cyber Intrusion'
date: 2025-11-19
permalink: /posts/2025/11/19/researchers-detail-tuoni-c2s-role-in-an-attempted-2025-real-estate-cyber-intrusion/
tags:
- veille-cyber
- hackernews
---
**Tentative d'intrusion dans le secteur immobilier par le biais du framework Tuoni**

Des chercheurs en cybersécurité ont mis en lumière une tentative d'attaque sophistiquée visant une entreprise immobilière américaine de premier plan. Cette intrusion a eu recours à Tuoni, un framework émergent de commande et de contrôle (C2) et de "red teaming", initialement conçu pour les professionnels de la sécurité et disponible gratuitement.

L'attaque, survenue mi-octobre 2025, a vraisemblablement débuté par de l'ingénierie sociale, utilisant potentiellement une imitation de Microsoft Teams pour obtenir un accès initial. L'acteur malveillant aurait usurpé l'identité de fournisseurs ou de collègues pour inciter un employé à exécuter une commande PowerShell.

Cette commande initiale servait à télécharger un second script PowerShell depuis un serveur externe ("kupaoquan[.]com"). Ce dernier utilisait des techniques de stéganographie pour dissimuler une charge utile dans une image bitmap (BMP). L'objectif principal était d'extraire et d'exécuter directement en mémoire un "shellcode", conduisant à l'activation de "TuoniAgent.dll". Cet agent communique ensuite avec un serveur C2, permettant un contrôle à distance de la machine compromise.

Des indices suggèrent une possible utilisation d'assistance par intelligence artificielle dans la génération du code du module de livraison initial, grâce à la structure modulaire et aux commentaires scriptés observés. Bien que l'attaque ait échoué, elle illustre l'abus continu d'outils de "red teaming" à des fins malveillantes.

**Points Clés :**

*   **Outil utilisé :** Framework Tuoni (C2 et "red teaming").
*   **Cible :** Une entreprise immobilière américaine.
*   **Méthode d'accès initiale suspectée :** Ingénierie sociale via imitation de Microsoft Teams.
*   **Techniques utilisées :** Exécution de scripts PowerShell, stéganographie (dissimulation dans des images BMP), exécution de code en mémoire, utilisation d'un agent (TuoniAgent.dll).
*   **Serveur C2 :** "kupaoquan[.]com".
*   **Indice d'assistance IA :** Génération de code observée dans le module initial.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est détaillée dans cet article concernant le framework Tuoni lui-même. L'attaque repose sur l'exploitation de l'ingénierie sociale et l'exécution de code par l'utilisateur.

**Recommandations :**

Bien que l'article ne fournisse pas de liste formelle de recommandations, les tactiques employées impliquent les mesures de sécurité suivantes :

*   **Sensibilisation à l'ingénierie sociale :** Former les employés à reconnaître et signaler les tentatives d'hameçonnage et les communications suspectes, y compris celles émanant de plateformes comme Microsoft Teams.
*   **Contrôle strict de l'exécution des scripts :** Mettre en place des politiques de sécurité qui restreignent l'exécution des scripts PowerShell provenant de sources non approuvées.
*   **Surveillance des activités réseau :** Détecter les communications vers des domaines ou des adresses IP potentiellement malveillants, tels que "kupaoquan[.]com".
*   **Analyse et détection des charges utiles en mémoire :** Utiliser des outils de sécurité capables de détecter et d'analyser les charges utiles exécutées directement en mémoire pour identifier les activités suspectes.
*   **Gestion rigoureuse des accès et des privilèges :** Limiter les privilèges des utilisateurs pour réduire l'impact potentiel d'une compromission.

---
[Source](https://thehackernews.com/2025/11/researchers-detail-tuoni-c2s-role-in.html){:target="_blank"}
