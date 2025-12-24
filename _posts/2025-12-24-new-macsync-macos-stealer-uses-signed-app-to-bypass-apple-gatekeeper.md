---
title: 'New MacSync macOS Stealer Uses Signed App to Bypass Apple Gatekeeper'
date: 2025-12-24
permalink: /posts/2025/12/24/new-macsync-macos-stealer-uses-signed-app-to-bypass-apple-gatekeeper/
tags:
- veille-cyber
- hackernews
---
**MacSync : une nouvelle menace furtive pour macOS**

Une nouvelle version du logiciel malveillant MacSync, conçu pour voler des informations sur macOS, a été découverte. Contrairement aux précédentes itérations, celle-ci utilise une application Swift signée numériquement et approuvée par Apple (notarisée) pour contourner les mécanismes de sécurité intégrés comme Gatekeeper.

Le logiciel malveillant se présente sous la forme d'un installateur d'application de messagerie. Bien qu'il soit signé et notarisé, il incite les utilisateurs à exécuter l'application d'une manière spécifique pour contourner ces protections. Une fois lancé, il procède à plusieurs vérifications, y compris la connectivité internet et une temporisation pour limiter la fréquence d'exécution, avant de télécharger et d'exécuter un script encodé. Des modifications dans la manière dont la commande `curl` est utilisée pour récupérer la charge utile suggèrent une volonté d'améliorer la fiabilité ou d'échapper à la détection.

Une technique d'évasion supplémentaire consiste à intégrer des documents PDF non pertinents dans le fichier DMG, gonflant sa taille pour le rendre moins suspect. La charge utile une fois décodée correspond à MacSync, une version renommée de Mac.c, apparue en avril 2025. MacSync intègre un agent Go qui va au-delà du simple vol de données, offrant des capacités de commande et de contrôle à distance.

Cette évolution reflète une tendance croissante chez les acteurs malveillants ciblant macOS, qui cherchent de plus en plus à utiliser des exécutables signés et notarisés pour se faire passer pour des applications légitimes.

**Points clés :**

*   Découverte d'une nouvelle variante du logiciel malveillant MacSync pour macOS.
*   Utilisation d'une application Swift signée numériquement et notarisée pour contourner Gatekeeper.
*   Distribution via un fichier DMG trompeur se faisant passer pour un installateur d'application de messagerie.
*   Mécanismes d'évasion incluant des instructions spécifiques pour l'exécution et l'ajout de fichiers non pertinents pour augmenter la taille du DMG.
*   Capacités étendues de vol de données et de commande/contrôle à distance.

**Vulnérabilités :**

*   La confiance accordée aux applications signées et notarisées par Apple, qui peut être exploitée si le certificat de signature est compromis ou si la technique d'exécution est contournée.

**Recommandations :**

*   Soyez extrêmement prudent lors du téléchargement et de l'exécution d'applications provenant de sources non officielles, même si elles semblent signées.
*   Mettez régulièrement à jour votre système d'exploitation macOS pour bénéficier des derniers correctifs de sécurité.
*   Utilisez un logiciel antivirus et antimalware réputé et maintenez-le à jour.
*   Soyez attentif aux instructions inhabituelles ou aux demandes de contournement des protections de sécurité lors de l'installation de logiciels.
*   Apple a révoqué le certificat de signature de code utilisé par cette campagne. Surveillez les mises à jour de sécurité d'Apple concernant Gatekeeper et XProtect.

---
[Source](https://thehackernews.com/2025/12/new-macsync-macos-stealer-uses-signed.html){:target="_blank"}
