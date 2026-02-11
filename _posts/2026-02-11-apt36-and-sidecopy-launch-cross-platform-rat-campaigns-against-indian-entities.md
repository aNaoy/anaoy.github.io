---
title: 'APT36 and SideCopy Launch Cross-Platform RAT Campaigns Against Indian Entities'
date: 2026-02-11
permalink: /posts/2026/02/11/apt36-and-sidecopy-launch-cross-platform-rat-campaigns-against-indian-entities/
tags:
- veille-cyber
- hackernews
---
**Campagnes Sophistiquées d'APT36 et SideCopy Ciblant l'Inde**

Des campagnes de cyberespionnage multiplateformes, attribuées aux groupes SideCopy et APT36 (aussi connu sous le nom de Transparent Tribe), ont récemment visé le secteur de la défense et les organisations gouvernementales indiennes. L'objectif est de compromettre les environnements Windows et Linux à l'aide de chevaux de Troie d'accès à distance (RAT) afin de dérober des données sensibles et d'assurer un accès persistant aux systèmes infectés.

**Points Clés :**

*   **Cible :** Le secteur indien de la défense, les organisations gouvernementales, ainsi que les secteurs de la politique, de la recherche et des infrastructures critiques.
*   **Acteurs :** APT36 et SideCopy, des groupes de menace alignés sur le Pakistan. SideCopy serait une subdivision de Transparent Tribe.
*   **Tactiques :** Utilisation d'e-mails de phishing avec des pièces jointes ou des liens malveillants comme vecteur d'infection initial. Exploitation de fichiers LNK (Windows), de binaires ELF (Linux) et de fichiers PowerPoint Add-In.
*   **Malware :** Déploiement de RAT tels que Geta RAT (Windows), Ares RAT (Linux) et DeskRAT (Windows/Golang).
*   **Objectifs :** Obtenir un accès à distance persistant, mener des reconnaissances système, collecter des données, exécuter des commandes et faciliter des opérations post-compromission à long terme.
*   **Évolution :** Les attaquants affinent leurs techniques en élargissant la couverture multiplateforme, en utilisant des techniques résidant en mémoire et en expérimentant de nouveaux vecteurs de livraison pour opérer discrètement.

**Vulnérabilités (Non spécifiées par CVE dans l'article) :**

L'article ne mentionne pas de CVE spécifiques. Les attaques reposent sur l'ingénierie sociale (phishing) et l'exécution de code malveillant via des fichiers d'apparence légitime (LNK, HTA, PowerPoint Add-Ins).

**Recommandations (Implicites) :**

*   **Vigilance accrue face au phishing :** Être particulièrement prudent avec les e-mails, les pièces jointes et les liens provenant de sources inconnues ou suspectes, surtout s'ils contiennent des thèmes liés à la défense.
*   **Sécurisation des endpoints :** Utiliser des solutions antivirus et anti-malware à jour et robustes pour détecter et bloquer les menaces.
*   **Mise à jour des systèmes :** S'assurer que les systèmes d'exploitation (Windows et Linux) et les logiciels (y compris les compléments PowerPoint) sont régulièrement mis à jour pour corriger les vulnérabilités connues.
*   **Formation des utilisateurs :** Sensibiliser les employés aux risques de cybersécurité, en particulier aux tactiques d'ingénierie sociale.
*   **Surveillance du réseau :** Mettre en place une surveillance continue pour détecter toute activité suspecte ou anormale sur le réseau.

---
[Source](https://thehackernews.com/2026/02/apt36-and-sidecopy-launch-cross.html){:target="_blank"}
