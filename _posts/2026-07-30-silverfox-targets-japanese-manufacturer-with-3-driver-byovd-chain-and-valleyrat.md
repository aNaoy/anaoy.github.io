---
title: 'SilverFox Targets Japanese Manufacturer with 3-Driver BYOVD Chain and ValleyRAT'
date: 2026-07-30
permalink: /posts/2026/07/30/silverfox-targets-japanese-manufacturer-with-3-driver-byovd-chain-and-valleyrat/
tags:
- veille-cyber
- hackernews
---
### Évolution des tactiques du groupe SilverFox : Utilisation d'une chaîne BYOVD à trois pilotes

Le groupe cybercriminel SilverFox cible le secteur industriel japonais avec une campagne sophistiquée visant à déployer le cheval de Troie d'accès à distance (RAT) **ValleyRAT**. L'attaque se distingue par l'utilisation combinée de techniques d'évasion avancées et une architecture modulaire hautement résiliente.

**Points clés :**
*   **Vecteur d'attaque :** Hameçonnage par e-mail (thématique de facturation) utilisant des services légitimes (QQ, Tencent Cloud) pour héberger des charges utiles.
*   **Technique BYOVD (Bring Your Own Vulnerable Driver) :** Utilisation de trois pilotes vulnérables distincts (`BootRepair.sys`, `EnPortv.sys` et `wsftprm.sys`) pour obtenir un accès au noyau et neutraliser les logiciels de sécurité.
*   **Persistance et résilience :** Mise en œuvre d'une architecture à double surveillance (watchdog) capable de restaurer automatiquement les composants malveillants si l'un d'eux est arrêté par un antivirus.
*   **Evasion :** Utilisation du "DLL sideloading" pour charger des bibliothèques malveillantes, combinée à une technique de "NTDLL unhooking" pour empêcher les solutions EDR de surveiller les appels API Windows.

**Vulnérabilités :**
*   Bien que les pilotes utilisés soient des logiciels signés légitimes, ils sont exploités en raison de leurs vulnérabilités connues de privilèges (BYOVD). Aucun identifiant CVE spécifique n'est mentionné pour ces pilotes, mais leur usage illustre le risque persistant lié à l'exécution de pilotes tiers obsolètes ou non sécurisés dans le noyau Windows.

**Recommandations :**
*   **Gestion des pilotes :** Implémenter et maintenir une liste blanche stricte des pilotes autorisés (via *Windows Defender Application Control* ou des solutions EDR) pour bloquer le chargement de pilotes vulnérables connus.
*   **Renforcement EDR :** Configurer les outils de sécurité pour détecter les comportements suspects liés au chargement de pilotes non signés ou suspects dans le répertoire système.
*   **Filtrage réseau :** Surveiller et bloquer les communications sortantes vers des infrastructures cloud publiques non autorisées ou suspectes, souvent utilisées pour le téléchargement de charges utiles (DLL sideloading).
*   **Sensibilisation :** Renforcer la vigilance face aux pièces jointes (archives ZIP) et aux liens hébergés sur des services cloud légitimes utilisés comme vecteurs d'entrée.

---
[Source](https://thehackernews.com/2026/07/silverfox-targets-japanese-manufacturer.html){:target="_blank"}
