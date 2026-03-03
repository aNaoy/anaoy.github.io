---
title: 'Fake Tech Support Spam Deploys Customized Havoc C2 Across Organizations'
date: 2026-03-03
permalink: /posts/2026/03/03/fake-tech-support-spam-deploys-customized-havoc-c2-across-organizations/
tags:
- veille-cyber
- hackernews
---
**Arnaque du support technique utilisant le framework Havoc C2**

Une nouvelle campagne d'attaques informatiques a été observée, durant laquelle des cybercriminels se font passer pour du support technique afin de déployer le framework de commande et contrôle (C2) Havoc. L'objectif final est généralement l'exfiltration de données ou le déploiement de rançongiciels. Les attaques débutent par des courriels de spam, suivis d'appels téléphoniques du faux support technique qui incitent les victimes à autoriser l'accès à distance à leur machine, soit via une session Quick Assist, soit en installant des outils comme AnyDesk. Une fois l'accès obtenu, les attaquants incitent la victime à visiter une fausse page web, se faisant passer pour Microsoft, afin de "mettre à jour" les règles anti-spam de Outlook. Cette démarche permet de collecter les identifiants de connexion de la victime et déclenche le téléchargement d'un prétendu correctif, qui est en réalité un exécutable malveillant. Ce dernier exploite des binaires légitimes pour charger une DLL conçue pour contourner les systèmes de détection et de réponse (EDR) et déployer le framework Havoc Demon. Les attaquants procèdent ensuite à des mouvements latéraux rapides au sein du réseau, établissant une persistance via des tâches planifiées ou l'utilisation d'outils de gestion à distance légitimes (RMM).

**Points clés :**

*   Utilisation d'une tactique d'ingénierie sociale par usurpation d'identité (faux support technique).
*   Déploiement du framework Havoc C2, souvent sous forme de "Demon agent".
*   Techniques d'évasion de défense avancées pour contourner les solutions de sécurité.
*   Mouvements latéraux rapides et stratégies de persistance multiples.
*   La méthode rappelle des tactiques précédemment associées à des groupes de rançongiciels comme Black Basta.

**Vulnérabilités / Techniques exploitées :**

*   **Ingénierie sociale :** Tromper les utilisateurs pour obtenir un accès initial et des identifiants.
*   **DLL Sideloading :** Exploitation de binaires légitimes pour charger des bibliothèques de liens dynamiques malveillantes.
*   **Contournement d'EDR :** Utilisation de techniques comme le Hell's Gate et le Halo's Gate pour intercepter et manipuler les fonctions du système d'exploitation (`ntdll.dll`).
*   **Obfuscation du flux de contrôle et boucles de délai basées sur le temps :** Pour rendre la détection plus difficile.
*   **Réutilisation d'outils légitimes :** Les outils RMM sont détournés pour assurer la persistance.

**Recommandations :**

*   **Sensibilisation des employés :** Former les utilisateurs à reconnaître les tentatives d'hameçonnage et les arnaques par téléphone se faisant passer pour du support technique.
*   **Vérification de l'identité :** Ne jamais accorder d'accès à distance ou fournir des informations confidentielles suite à une demande non sollicitée, même si elle semble provenir d'une source légitime. Vérifier l'identité de la personne via un canal de communication différent et connu.
*   **Gestion des accès et privilèges :** Appliquer le principe du moindre privilège et segmenter le réseau pour limiter la propagation des menaces.
*   **Surveillance et détection :** Mettre en place des solutions de sécurité robustes et surveiller activement les journaux pour détecter les activités suspectes, y compris les tentatives de contournement d'EDR.
*   **Mises à jour et gestion des correctifs :** S'assurer que tous les systèmes et logiciels sont régulièrement mis à jour pour corriger les vulnérabilités connues.
*   **Analyse des outils RMM :** Auditer et sécuriser l'utilisation des outils RMM, en s'assurant qu'ils ne sont utilisés que par du personnel autorisé et qu'ils disposent de mécanismes de sécurité adéquats.

---
[Source](https://thehackernews.com/2026/03/fake-tech-support-spam-deploys.html){:target="_blank"}
