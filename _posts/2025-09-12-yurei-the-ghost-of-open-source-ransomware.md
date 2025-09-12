---
title: 'Yurei & The Ghost of Open Source Ransomware'
date: 2025-09-12
permalink: /posts/2025/09/12/yurei-the-ghost-of-open-source-ransomware/
tags:
- veille-cyber
- zerodaysfans
---
## Yurei : Une Nouvelle Menace Ransomware Issue de l'Open Source

Un nouveau groupe de ransomware, nommé Yurei, a émergé, utilisant une souche basée sur le code open source de Prince-Ransomware. Cette approche réduit considérablement la barrière à l'entrée pour les cybercriminels, leur permettant de lancer des opérations de ransomware avec des compétences techniques limitées. Yurei opère selon un modèle de double extorsion : il crypte les fichiers des victimes tout en dérobant des données sensibles, puis exige une rançon pour la restauration des fichiers et la non-divulgation des informations volées.

### Points Clés

*   **Mise en œuvre rapide :** Le groupe Yurei a été identifié pour la première fois le 5 septembre et a rapidement listé trois victimes, dont une entreprise de fabrication alimentaire sri-lankaise.
*   **Origine Open Source :** Le ransomware Yurei est une adaptation mineure de Prince-Ransomware, un projet open source écrit en Go. Cette facilité d'accès démocratise le ransomware pour des acteurs moins qualifiés.
*   **Double Extorsion :** Yurei combine le chiffrement des données avec le vol et la menace de publication d'informations sensibles pour maximiser la pression sur les victimes.
*   **Vulnérabilité Potentielle :** Le ransomware Yurei présente une faille dans sa gestion des copies d'ombre (Shadow Copies), potentiellement permettant une récupération partielle des fichiers.
*   **Origines possibles :** Des indices suggèrent que les auteurs du ransomware pourraient être basés au Maroc.

### Vulnérabilités

*   **Dépendance à Prince-Ransomware :** Le ransomware Yurei hérite des défauts de son parent open source.
*   **Absence de suppression des Shadow Copies :** La technique courante des ransomwares de supprimer les copies d'ombre du Volume Shadow Copy Service (VSS) n'est pas implémentée. Si VSS est activé, les victimes pourraient potentiellement restaurer leurs fichiers sans payer.
*   **Absence de fonctions anti-analyse :** Les échantillons analysés ne montrent pas de techniques d'obfuscation ou de protection contre l'analyse, et conservent même les symboles du compilateur, facilitant l'ingénierie inverse.
*   **Configuration de fond d'écran défaillante :** La tentative de modifier le fond d'écran de Windows échoue, laissant un fond unicolore, ce qui témoigne d'un manque de finition.

Il n'y a pas de CVE spécifiques mentionnés pour Yurei ou Prince-Ransomware dans cet article.

### Recommandations

*   **Activation et surveillance des Shadow Copies (VSS) :** Activer le service de cliché instantané des volumes et prendre régulièrement des instantanés peut permettre une récupération partielle des données chiffrées.
*   **Défenses proactives :** L'article mentionne que Check Point Threat Emulation et Harmony Endpoint offrent une couverture contre les tactiques, types de fichiers et systèmes d'exploitation décrits.
*   **Surveillance et détection :** La nature open source de ce ransomware signifie que les variations sont plus faciles à détecter pour les défenseurs disposant des bons outils et de l'intelligence sur les menaces.
*   **Prudence face à l'open source :** Les organisations doivent être conscientes que les projets open source peuvent être rapidement réutilisés et modifiés par des acteurs malveillants, réduisant ainsi leur effort de développement.

---
[Source](https://research.checkpoint.com/2025/yurei-the-ghost-of-open-source-ransomware/){:target="_blank"}
