---
title: 'A USB worm’s second life: Retadup spreading CoffeeLoader'
date: 2026-11-16
permalink: /posts/2026/11/16/a-usb-worms-second-life-retadup-spreading-coffeeloader/
tags:
- veille-cyber
- securelist
---
### Résurgence du ver Retadup : Propagation du Trojan CoffeeLoader

Le ver informatique Retadup, officiellement neutralisé en 2019, a été réactivé en 2024 via le rachat de ses anciens noms de domaine de serveurs de commande (C2). Cette infrastructure est désormais utilisée pour distribuer une nouvelle variante du malware CoffeeLoader.

#### Points clés
*   **Mécanisme de propagation :** Retadup se propage via des supports USB amovibles en utilisant des fichiers LNK malveillants. Une fois actif, il télécharge et exécute des charges utiles tierces, dont CoffeeLoader.
*   **Évolution du packer Armoury :** La nouvelle variante du packer utilise désormais la bibliothèque OpenGL (au lieu d'OpenCL) pour exploiter les capacités du GPU lors du déchiffrement du code malveillant.
*   **Chaîne d'infection :** L'installeur (NSIS) déploie une bibliothèque `7z.dll` corrompue qui exécute un shellcode décryptant le chargeur de CoffeeLoader. Ce dernier assure la persistance via le registre Windows (`Run`) et empêche la désactivation du démarrage automatique via le Gestionnaire des tâches.
*   **Ciblage :** Bien que l'échelle soit plus réduite qu'en 2019 (environ 15 000 systèmes touchés), l'infection reste active, principalement au Pérou, en Angola, en Russie et en Bolivie.

#### Vulnérabilités
*   **Abus de fonctionnalités légitimes :** Utilisation de `rundll32.exe` pour charger des bibliothèques malveillantes et exploitation des clés de registre d'autorun (`Run`).
*   **Injection de processus :** Le malware injecte son code dans des processus légitimes (ex: `dllhost.exe`, `svchost.exe`, `WerFault.exe`) pour dissimuler son activité réseau.

#### Recommandations
*   **Restriction des supports USB :** Désactiver l'exécution automatique des périphériques amovibles et limiter l'accès USB dans les environnements professionnels.
*   **Surveillance des processus :** Surveiller les comportements anormaux liés au lancement de `rundll32.exe` à partir de répertoires suspects dans `%PROGRAMDATA%` ou `%LOCALAPPDATA%`.
*   **Filtrage réseau :** Bloquer les connexions vers les domaines C2 identifiés (ex: `alphanoob[.]com`, `newblackage[.]com`, `internet-speed-check[.]com`).
*   **Hygiène système :** Maintenir les solutions EDR/Antivirus à jour pour détecter les signatures des nouveaux shellcodes et les tentatives d'injection de processus.

---
[Source](https://securelist.com/retadup-delivers-coffeeloader/121908/){:target="_blank"}
