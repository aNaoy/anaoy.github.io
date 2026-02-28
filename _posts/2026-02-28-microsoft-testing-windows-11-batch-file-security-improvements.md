---
title: 'Microsoft testing Windows 11 batch file security improvements'
date: 2026-02-28
permalink: /posts/2026/02/28/microsoft-testing-windows-11-batch-file-security-improvements/
tags:
- veille-cyber
- bleepingcomp
---
**Renforcement de la sécurité des scripts batch sous Windows 11**

Microsoft introduit de nouvelles améliorations de sécurité et de performance pour l'exécution des fichiers batch et des scripts CMD dans les versions Insider Preview de Windows 11.

**Points Clés :**

*   Une nouvelle option permet de verrouiller les fichiers batch pendant leur exécution, les empêchant d'être modifiés.
*   Cette fonctionnalité vise à renforcer la sécurité et à optimiser les performances dans les environnements d'entreprise.
*   Elle améliore la validation des signatures en la réalisant une seule fois au lieu de pour chaque instruction.
*   Des améliorations ont également été apportées à la fonctionnalité de partage audio, permettant des contrôles de volume individuels et une meilleure indication visuelle des sessions actives.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans cet article concernant cette mise à jour. L'amélioration vise à prévenir des modifications potentielles de scripts qui pourraient introduire des risques de sécurité.

**Recommandations :**

*   Les administrateurs système peuvent activer le mode de traitement sécurisé des fichiers batch en ajoutant la valeur de registre `LockBatchFilesInUse` sous `HKEY_LOCAL_MACHINE\Software\Microsoft\Command Processor`.
*   Les auteurs de politiques d'application peuvent activer ce mode via le contrôle de manifeste d'application `LockBatchFilesWhenInUse`.
*   Les utilisateurs disposant des builds Insider Preview appropriées devraient observer ces améliorations.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-testing-windows-11-batch-file-security-improvements/){:target="_blank"}
