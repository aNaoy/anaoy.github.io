---
title: 'Sandworm-Linked UAC-0145 Uses Fake Job Interviews to Push VPN That Can Run Commands'
date: 2026-08-11
permalink: /posts/2026/08/11/sandworm-linked-uac-0145-uses-fake-job-interviews-to-push-vpn-that-can-run-commands/
tags:
- veille-cyber
- hackernews
---
### Espionnage via de faux entretiens d'embauche : la campagne du groupe UAC-0145

Le groupe d'acteurs de menaces **UAC-0145**, une sous-structure de **Sandworm** (affilié au GRU russe), orchestre une campagne d'ingénierie sociale sophistiquée visant des informaticiens ukrainiens sous couvert de fausses opportunités professionnelles.

**Points clés :**
* **Méthodologie :** Les attaquants contactent leurs cibles sur des sites d'emploi, déplacent la conversation sur Telegram, puis organisent des entretiens vidéo sur Zoom (parfois avec des avatars générés par IA).
* **Vecteur d'attaque :** Lors d'un prétendu test technique, les victimes sont incitées à installer un client VPN personnalisé (« SopraVPN ») hébergé sur SourceForge, se faisant passer pour un logiciel légitime de l'entreprise Sopra Steria.
* **Mécanisme malveillant :** Le VPN est une version modifiée de WireGuard intégrant une porte dérobée. Il permet l'exécution de commandes arbitraires via des scripts PowerShell (`PostUp`) ou des téléchargements de charges utiles secondaires à l'insu de l'utilisateur.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur une **exécution volontaire de code malveillant (Backdoor)** par l'utilisateur, facilitée par une modification malveillante du code source open-source de WireGuard.

**Recommandations :**
* **Vérification des logiciels :** Ne télécharger et n'installer que des outils VPN provenant de sources officielles et vérifiées. Se méfier des logiciels « sur mesure » fournis par des recruteurs dans un contexte de test technique.
* **Gestion des accès :** Restreindre l'accès aux ressources de l'entreprise uniquement aux appareils gérés et supervisés par les services informatiques de l'organisation.
* **Sécurité des terminaux :** Déployer des solutions de sécurité (EDR/antivirus) capables de détecter les comportements anormaux, les tâches planifiées suspectes et l'exécution de scripts PowerShell non autorisés.
* **Sensibilisation :** Former les employés aux tactiques d'ingénierie sociale, particulièrement lors des processus de recrutement en ligne.

---
[Source](https://thehackernews.com/2026/08/sandworm-linked-uac-0145-uses-fake-job.html){:target="_blank"}
