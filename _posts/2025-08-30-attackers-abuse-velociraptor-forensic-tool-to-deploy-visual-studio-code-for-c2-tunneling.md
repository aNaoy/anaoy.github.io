---
title: 'Attackers Abuse Velociraptor Forensic Tool to Deploy Visual Studio Code for C2 Tunneling'
date: 2025-08-30
permalink: /posts/2025/08/30/attackers-abuse-velociraptor-forensic-tool-to-deploy-visual-studio-code-for-c2-tunneling/
tags:
- veille-cyber
- hackernews
---
**Utilisation Malveillante d'Outils Légitimes : Nouvelle Tactique d'Attaque**

Des acteurs de la menace exploitent désormais des outils de cybersécurité légitimes pour mener des cyberattaques sophistiquées. Une récente observation révèle l'utilisation de Velociraptor, un outil de surveillance et d'analyse forensique, pour établir des tunnels de commande et de contrôle (C2) via Visual Studio Code. Cette approche s'inscrit dans une évolution des tactiques, les attaquants cherchant à minimiser le déploiement de leurs propres malwares en tirant parti de solutions existantes.

L'attaque débute par l'utilisation de l'utilitaire Windows `msiexec` pour télécharger un installeur MSI depuis un domaine Cloudflare Workers. Ce fichier déploie Velociraptor, qui contacte ensuite un autre domaine Cloudflare. L'accès ainsi obtenu est utilisé pour télécharger et exécuter Visual Studio Code, avec l'option de tunneling activée, permettant le contrôle à distance et l'exécution de code. Des payloads supplémentaires sont également téléchargés via `msiexec`.

Parallèlement, des campagnes d'attaques exploitent Microsoft Teams pour obtenir un accès initial, usurpant l'identité de services d'assistance informatique pour inciter les utilisateurs à installer des logiciels d'administration à distance (AnyDesk, Radmin, etc.) ou à livrer des payloads malveillants via PowerShell. Ces tactiques visent le vol d'informations d'identification et l'établissement de persistance.

Une autre méthode observée combine des liens Office.com légitimes avec Active Directory Federation Services (ADFS) pour rediriger les utilisateurs vers de fausses pages de connexion Microsoft 365, dans le but de voler des identifiants.

**Points Clés :**

*   **Abus d'Outils Légitimes :** Exploitation de Velociraptor, Visual Studio Code, et de plateformes de collaboration comme Microsoft Teams.
*   **Tactiques "Living off the Land" (LotL) :** Utilisation d'utilitaires Windows natifs comme `msiexec`.
*   **Tunneling C2 :** Utilisation de Visual Studio Code pour établir des canaux de communication avec des serveurs contrôlés par les attaquants.
*   **Usurpation d'Identité :** Imitation de services d'assistance informatique via Microsoft Teams pour l'ingénierie sociale.
*   **Phishing Avancé :** Exploitation d'ADFS pour rediriger vers des pages de connexion frauduleuses.

**Vulnérabilités Potentielles :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article, mais l'article souligne la capacité des attaquants à exploiter la configuration d'ADFS pour héberger leurs propres pages de phishing, ce qui rend les détections basées sur les URL plus difficiles.

**Recommandations :**

*   Surveiller et investiguer l'utilisation non autorisée de Velociraptor.
*   Traiter l'observation de ces méthodes comme un précurseur potentiel de ransomware.
*   Mettre en œuvre des systèmes de détection et de réponse sur les endpoints (EDR).
*   Surveiller les outils inattendus et les comportements suspects.
*   Appliquer les meilleures pratiques de sécurisation des systèmes et maintenir des sauvegardes régulières.
*   Surveiller les journaux d'audit de Microsoft Teams (ChatCreated, MessageSent) et enrichir les signaux avec des données contextuelles.
*   Former les utilisateurs à identifier les usurpations d'identité de services d'assistance informatique.

---
[Source](https://thehackernews.com/2025/08/attackers-abuse-velociraptor-forensic.html){:target="_blank"}
