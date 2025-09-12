---
title: 'New HybridPetya ransomware can bypass UEFI Secure Boot'
date: 2025-09-12
permalink: /posts/2025/09/12/new-hybridpetya-ransomware-can-bypass-uefi-secure-boot/
tags:
- veille-cyber
- bleepingcomp
---
## HybridPetya : Une Nouvelle Menace Infectant les Systèmes via le Démarrage UEFI

Une nouvelle variante de rançongiciel, baptisée HybridPetya, a été découverte. Elle est capable de contourner la fonctionnalité de démarrage sécurisé UEFI (UEFI Secure Boot) pour installer un logiciel malveillant dans la partition système EFI.

Ce rançongiciel s'inspire des malwares destructeurs Petya/NotPetya des années 2016 et 2017, qui chiffraient des ordinateurs et empêchaient leur démarrage. Contrairement à ses prédécesseurs, HybridPetya ne semble pas proposer d'option de récupération. Les chercheurs estiment qu'il pourrait s'agir d'un projet de recherche, d'une preuve de concept ou d'une version préliminaire d'un outil de cybercriminalité en phase de test.

La présence de ce type de logiciel malveillant, capable de s'exécuter avant le système d'exploitation, souligne une menace croissante pour la sécurité des systèmes informatiques.

### Points Clés

*   **Exploitation du démarrage UEFI :** HybridPetya cible la partition système EFI (ESP) pour s'installer et s'exécuter avant le système d'exploitation.
*   **Contournement du démarrage sécurisé :** Il utilise une vulnérabilité pour désactiver ou contourner le démarrage sécurisé UEFI, empêchant ainsi les protections natives de bloquer son exécution.
*   **Inspiration de Petya/NotPetya :** Le rançongiciel reprend l'apparence et la chaîne d'attaque des anciens malwares Petya et NotPetya.
*   **Chiffrement des données :** Une fois actif, il chiffre les données du système et affiche un faux message de vérification de disque (CHKDSK) pour masquer ses actions.
*   **Demande de rançon :** Après le chiffrement, une note de rançon apparaît, exigeant un paiement en Bitcoin pour la récupération des fichiers.
*   **Mécanisme de récupération (potentiel) :** Le malware sauvegarde le chargeur de démarrage Windows original, potentiellement pour le restaurer après paiement de la rançon.

### Vulnérabilités

*   **CVE-2024-7344 :** Cette vulnérabilité permet à des applications signées par Microsoft d'être exploitées pour déployer des bootkits, même lorsque le démarrage sécurisé est activé.

### Recommandations

*   **Appliquer les mises à jour de sécurité :** Maintenir les systèmes d'exploitation à jour, notamment en installant les correctifs de sécurité mensuels de Microsoft, protège contre des vulnérabilités comme la CVE-2024-7344.
*   **Sauvegardes hors ligne :** Conserver des sauvegardes régulières et hors ligne des données critiques permet une restauration aisée en cas d'attaque par rançongiciel.
*   **Surveillance des indicateurs de compromission (IoC) :** Les chercheurs ont rendu disponibles des IoC pour aider à la détection et à la défense contre cette menace.

---
[Source](https://www.bleepingcomputer.com/news/security/new-hybridpetya-ransomware-can-bypass-uefi-secure-boot/){:target="_blank"}
