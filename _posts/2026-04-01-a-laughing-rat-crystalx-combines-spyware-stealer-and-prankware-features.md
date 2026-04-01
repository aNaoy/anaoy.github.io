---
title: 'A laughing RAT: CrystalX combines spyware, stealer, and prankware features'
date: 2026-04-01
permalink: /posts/2026/04/01/a-laughing-rat-crystalx-combines-spyware-stealer-and-prankware-features/
tags:
- veille-cyber
- securelist
---
### CrystalX : Une menace hybride entre RAT, stealer et "prankware"

CrystalX est un nouveau cheval de Troie d'accès à distance (RAT) distribué sous forme de Malware-as-a-Service (MaaS) via des canaux Telegram. Dérivé du code de *WebRAT* (ou *Salat Stealer*), il se distingue par un arsenal complet combinant espionnage classique et fonctionnalités de harcèlement (prankware).

#### Points clés
*   **Architecture :** Développé en Go, le malware est distribué via un panneau de contrôle complet permettant une configuration à la carte (géoblocage, anti-analyse, icônes personnalisées).
*   **Polyvalence :** En plus des fonctions de RAT (accès distant VNC, capture audio/vidéo, exécution de commandes), il intègre un *stealer* (vol de données navigateurs, Steam, Discord, Telegram), un *keylogger* et un *clipper* (substitution d'adresses de portefeuilles crypto dans le presse-papier).
*   **Composante "Prankware" :** Le panneau dispose d'une section "Rofl" permettant des actions intrusives : rotation d'écran, inversion des clics souris, blocage du clavier/souris ou affichage de messages à la victime.
*   **Persistance :** Le malware est en développement actif. Bien que les tentatives d'infection observées se concentrent actuellement sur la Russie, sa nature de service global permet des déploiements partout dans le monde.

#### Vulnérabilités et mécanismes de défense
Aucune CVE spécifique n'est exploitée ; le malware utilise des techniques de contournement pour rester furtif :
*   **Anti-analyse :** Détection de machines virtuelles et de proxys, vérification de processus de sécurité (Fiddler, Burp Suite), et boucles de vérification anti-débogage.
*   **Furtivité :** Patchs pour les fonctions systèmes `AmsiScanBuffer`, `EtwEventWrite` et `MiniDumpWriteDump` afin d'échapper à la détection EDR/Antivirus.
*   **Chiffrement :** Utilisation de l'algorithme ChaCha20 avec une clé codée en dur.

#### Recommandations
*   **Surveillance réseau :** Bloquer les connexions vers les domaines associés au C2 : `webcrystal[.]lol`, `webcrystal[.]sbs` et `crystalxrat[.]top`.
*   **Détection EDR :** Surveiller la création suspecte de répertoires dans `%TEMP%` ou `%LOCALAPPDATA%\Microsoft\Edge\ExtSvc`, souvent utilisés pour l'injection de scripts malveillants (clipper).
*   **Analyse comportementale :** Être vigilant face à des comportements anormaux sur les postes de travail tels que le redémarrage impestif des pilotes d'entrée (souris/clavier) ou des modifications soudaines de l'affichage, signes typiques des fonctionnalités de harcèlement de ce malware.
*   **Hygiène logicielle :** Désactiver l'exécution de scripts non signés dans les navigateurs et maintenir les solutions de sécurité à jour pour détecter les nouveaux implants via leurs signatures.

---
[Source](https://securelist.com/crystalx-rat-with-prankware-features/119283/){:target="_blank"}
