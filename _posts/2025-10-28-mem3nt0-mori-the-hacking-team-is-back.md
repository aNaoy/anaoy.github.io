---
title: 'Mem3nt0 mori – The Hacking Team is back!'
date: 2025-10-28
permalink: /posts/2025/10/28/mem3nt0-mori-the-hacking-team-is-back/
tags:
- veille-cyber
- securelist
---
**Le Retour du Spyware : Dante et l'Opération ForumTroll**

Une campagne d'infection sophistiquée, nommée Opération ForumTroll, a été détectée en mars 2025. Les attaques utilisaient des liens de phishing personnalisés et de courte durée, envoyés par e-mail, qui déclenchaient des infections simplement en étant visités via un navigateur basé sur Chromium.

**Points Clés:**

*   **Mode d'infection :** Les victimes sont infectées en cliquant sur un lien de phishing personnalisé qui les dirige vers un site web malveillant.
*   **Objectif :** L'espionnage semble être le but principal de cette opération.
*   **Attribution :** Les analyses ont permis de remonter à un logiciel espion commercial nommé "Dante", développé par Memento Labs, une entreprise anciennement connue sous le nom de Hacking Team. Les similitudes de code suggèrent que l'Opération ForumTroll a été menée avec des outils issus de Memento Labs.
*   **Ciblage :** Les leurres d'e-mails visaient des médias, universités, centres de recherche, organisations gouvernementales et institutions financières en Russie.

**Vulnérabilités:**

*   **CVE-2025-2783 :** Une vulnérabilité zero-day dans Google Chrome qui permettait une évasion de sandbox sans actions malveillantes évidentes. L'exploitation reposait sur un défaut logique lié à la gestion des "pseudo-handles" de la fonction `GetCurrentThread` par l'API `DuplicateHandle` sous Windows.
*   **CVE-2025-2857 :** Une vulnérabilité similaire découverte dans Firefox.

**Composants de l'Attaque:**

*   **Phishing Email :** Des e-mails d'invitation personnalisés pour le forum "Primakov Readings" ont été utilisés pour inciter les victimes à cliquer sur les liens.
*   **Validator :** Un script exécuté par le navigateur pour valider l'utilisateur et télécharger la prochaine étape de l'attaque. Il utilise l'API WebGPU pour un calcul SHA-256 et l'algorithme ECDH pour l'échange de clés.
*   **Sandbox Escape Exploit :** Un exploit pour Chrome (CVE-2025-2783) utilisant une faille dans la gestion des pseudo-handles pour exécuter du code dans le processus du navigateur.
*   **Persistent Loader :** Utilise le détournement d'objets COM pour assurer la persistance du malware. Il masque le code principal avec OLLVM et un encodeur binaire, puis le déchiffre avec une version modifiée de ChaCha20.
*   **LeetAgent :** Le logiciel espion principal utilisé dans la campagne ForumTroll, caractérisé par des commandes en "leetspeak". Il réalise des opérations de keylogging et de vol de fichiers. Il communique via HTTPS et utilise l'infrastructure cloud Fastly.net pour ses serveurs C2.
*   **Dante :** Un spyware commercial plus sophistiqué découvert lors de l'analyse d'attaques antérieures attribuées au même groupe. Il utilise des techniques avancées d'anti-analyse (VMProtect, détection de debug, anti-hooking, vérification d'environnement, anti-sandbox). Les commandes et la configuration sont chiffrées.

**Recommandations:**

*   **Surveillance des pseudo-handles :** Les développeurs d'applications privilégiées et les systèmes d'exploitation devraient renforcer la sécurité de l'API `DuplicateHandle` en vérifiant la validité des pseudo-handles fournis.
*   **Méfiance face aux e-mails de phishing :** Rester vigilant face aux e-mails d'invitation personnalisés, même s'ils semblent légitimes.
*   **Mises à jour régulières des navigateurs :** Maintenir les navigateurs web à jour est crucial pour bénéficier des correctifs de sécurité.
*   **Recherche sur les spyware commerciaux :** La découverte de Dante souligne l'importance de la recherche continue sur le marché des spyware commerciaux et leurs potentiels usages malveillants.
*   **Indicateurs de Compromission (IoCs) :** Utiliser les IoCs fournis, notamment les noms de dossiers et de fichiers spécifiques utilisés par Dante, pour identifier les infections actives.

---
[Source](https://securelist.com/forumtroll-apt-hacking-team-dante-spyware/117851/){:target="_blank"}
