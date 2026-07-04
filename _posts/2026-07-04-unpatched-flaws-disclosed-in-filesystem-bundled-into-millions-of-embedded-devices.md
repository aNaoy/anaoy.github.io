---
title: 'Unpatched Flaws Disclosed in Filesystem Bundled Into Millions of Embedded Devices'
date: 2026-07-04
permalink: /posts/2026/07/04/unpatched-flaws-disclosed-in-filesystem-bundled-into-millions-of-embedded-devices/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans la bibliothèque FatFs : un risque majeur pour l'IoT

Sept vulnérabilités ont été identifiées dans **FatFs**, une bibliothèque logicielle omniprésente utilisée dans des millions d'appareils embarqués (caméras, drones, contrôleurs industriels, portefeuilles crypto) pour lire les formats FAT/exFAT. L'absence de maintenance active de la bibliothèque complique la correction de ces failles, exposant les systèmes à des risques d'exécution de code arbitraire via l'insertion de supports de stockage piégés (USB/SD) ou de mises à jour malveillantes.

**Points clés :**
*   **Risque élevé :** Les appareils embarqués manquent souvent de protections mémoire, permettant un contrôle total du système via une simple injection de données mal formées.
*   **Absence de correctif :** Le développeur principal de FatFs est injoignable, laissant la charge du colmatage aux fabricants utilisant cette bibliothèque (ex: ESP-IDF, STM32Cube, Zephyr, etc.).
*   **Automatisation des menaces :** Ces failles ont été découvertes par des agents IA, soulignant que des attaquants disposent désormais de moyens simplifiés pour identifier des vulnérabilités complexes.

**Vulnérabilités répertoriées :**
*   **CVE-2026-6682 (7.6) :** Dépassement d'entier lors du montage FAT32, entraînant une corruption mémoire et exécution de code.
*   **CVE-2026-6687 (7.6) :** Dépassement de tampon sur les labels de volume exFAT.
*   **CVE-2026-6688 (7.6) :** Dépassement lié aux noms de fichiers longs dans les wrappers entourant FatFs.
*   **CVE-2026-6685 (6.1) :** Corruption silencieuse de données sur volumes fragmentés.
*   **CVE-2026-6683 (4.6) :** Division par zéro causant le plantage (brick) de l'appareil.
*   **CVE-2026-6686 (4.6) :** Fuite de données résiduelles provenant de fichiers supprimés.
*   **CVE-2026-6684 (4.6) :** Blocage au montage via une table de partition GPT malformée (seule faille corrigée dans la version R0.16).

**Recommandations :**
*   **Pour les développeurs firmware :** Auditer le code enveloppant (wrapper) la bibliothèque FatFs, sécuriser strictement le traitement des tailles de fichiers et des noms de fichiers, et mettre en place des patchs personnalisés sans attendre une mise à jour amont.
*   **Pour les utilisateurs finaux :** Restreindre physiquement l'accès aux ports USB/SD des appareils sensibles et surveiller activement la publication de mises à jour de firmware par les constructeurs.

---
[Source](https://thehackernews.com/2026/07/unpatched-flaws-disclosed-in-filesystem.html){:target="_blank"}
