---
title: 'Cracking ValleyRAT: From Builder Secrets to Kernel Rootkits'
date: 2025-12-10
permalink: /posts/2025/12/10/cracking-valleyrat-from-builder-secrets-to-kernel-rootkits/
tags:
- veille-cyber
- zerodaysfans
---
## ValleyRAT: De l'Outil de Création aux Rootkits Kernel

L'analyse approfondie de ValleyRAT, une porte dérobée modulaire également connue sous le nom de Winos/Winos4.0, révèle des techniques avancées de la part de ses développeurs. L'accès aux fichiers de développement de cet outil, bien que sans le code source complet, a permis de reconstituer la fonctionnalité de ses principaux modules.

Parmi les composants les plus préoccupants figure un plugin embarquant un rootkit kernel-mode. Celui-ci, malgré son ancienneté, parvient à rester chargé et fonctionnel sur des systèmes Windows 11 à jour, contournant les protections intégrées. Ses capacités incluent l'installation furtive de pilotes, l'injection de code en mode utilisateur via APC, et la suppression forcée de logiciels de sécurité (AV/EDR).

L'étude des données de détection confirme une augmentation significative de l'utilisation de ValleyRAT, avec environ 85% des échantillons observés au cours des six derniers mois, coïncidant avec la publication publique de son outil de création. Cette accessibilité accrue complique l'attribution des attaques à des acteurs spécifiques, comme ceux précédemment associés à ce malware.

### Points Clés :

*   **Architecture Modulaire Avancée :** ValleyRAT est construit autour d'un système de plugins permettant une grande flexibilité.
*   **Rootkit Kernel-Mode Sophistiqué :** Le "Driver Plugin" intègre un rootkit capable de contourner les sécurités modernes de Windows.
*   **Installation Furtive et Suppression d'AV/EDR :** Le rootkit peut s'installer discrètement et éliminer les défenses.
*   **Injection de Shellcode via APC :** Une méthode d'injection avancée est utilisée pour exécuter du code malveillant.
*   **Disponibilité Publique du Builder :** L'outil de création de ValleyRAT est désormais accessible, facilitant son adoption par divers acteurs.
*   **Attribution Compliquée :** La diffusion publique rend difficile l'identification des auteurs des attaques.

### Vulnérabilités (CVEs) :

L'article ne détaille pas de CVEs spécifiques directement exploitées, mais met en évidence l'exploitation de failles de conception ou d'implémentation dans le système d'exploitation et les mécanismes de signature de pilotes. Le rootkit tire parti de la politique de signature de pilotes de Windows, permettant le chargement de pilotes avec des certificats expirés sous certaines conditions.

### Recommandations :

*   **Surveillance et Détection :** Mettre en place des règles de détection robustes pour identifier les modules ValleyRAT et les comportements associés (installation de pilotes suspects, communications C2, suppression de fichiers, injection de processus).
*   **Application des Correctifs de Sécurité :** Bien que le rootkit puisse contourner certaines protections, maintenir les systèmes à jour reste essentiel.
*   **Gestion Rigoureuse des Pilotes :** Surveiller l'installation de pilotes inconnus ou non signés par des sources de confiance.
*   **Analyse Comportementale :** Utiliser des solutions de sécurité capables de détecter les comportements anormaux plutôt que de se fier uniquement aux signatures.
*   **Éducation et Sensibilisation :** Informer les utilisateurs sur les risques liés aux malwares et aux techniques d'ingénierie sociale qui pourraient accompagner le déploiement de ce type d'outil.
*   **Investigation des Certificats Expirés :** Porter une attention particulière aux pilotes signés avec des certificats expirés, même s'ils sont techniquement chargés.

---
[Source](https://research.checkpoint.com/2025/cracking-valleyrat-from-builder-secrets-to-kernel-rootkits/){:target="_blank"}
