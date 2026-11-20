---
title: 'ROMULUS ClickFix Attacks Deliver RAT That Can Spy on Users and Control PCs'
date: 2026-11-20
permalink: /posts/2026/11/20/romulus-clickfix-attacks-deliver-rat-that-can-spy-on-users-and-control-pcs/
tags:
- veille-cyber
- hackernews
---
### ROMULUS : Une plateforme de distribution de RAT via les attaques ClickFix

La plateforme **ROMULUS** est utilisée par des cybercriminels pour propager des logiciels malveillants, notamment le cheval de Troie d'accès à distance (RAT) **CNCMachineRMS** et le chargeur **Legion Loader**. Ces attaques s'appuient sur des leurres de type « ClickFix », incitant les utilisateurs à copier-coller des commandes malveillantes ou à exécuter des fichiers infectés sous de faux prétextes (vérification CAPTCHA, outils de mise à jour, etc.).

#### Points clés
*   **Méthodologie :** Utilisation de la technique de *DLL sideloading* via des installateurs MSI piégés (masqués en outils légitimes) ou des commandes PowerShell.
*   **Capacités du RAT :** Le logiciel malveillant permet un contrôle total de la machine (prise de contrôle à distance, capture d'écran, accès micro/caméra, exécution de charges utiles secondaires).
*   **Communication :** Le pilotage des machines compromises s'effectue via le protocole DNS over HTTPS (DoH) pour contourner les mécanismes de détection réseau classiques.
*   **Diversification :** Les attaques ClickFix sont devenues omniprésentes, utilisant des publicités Google (malvertising), des sites WordPress compromis, des faux profils ChatGPT et des techniques de redirection complexes pour piéger les utilisateurs Windows et macOS.

#### Vulnérabilités exploitées
Bien qu'aucune CVE spécifique ne soit citée, les vecteurs d'attaque reposent sur :
*   **Abus de fonctionnalités système :** Détournement du fonctionnement légitime de `msiexec.exe`, du terminal Windows/macOS et de l'utilitaire `finger`.
*   **DLL Sideloading :** Exploitation de la confiance accordée par le système d'exploitation à des exécutables signés numériquement (ex: IBM SPSS IDE) pour charger des bibliothèques malveillantes.

#### Recommandations
*   **Vigilance sur les interactions :** Ne jamais copier-coller des commandes provenant de pages Web, même si elles apparaissent dans des fenêtres de vérification de sécurité (type Cloudflare ou CAPTCHA).
*   **Gestion des privilèges :** Éviter l'exécution de fichiers MSI ou de scripts provenant de sources non vérifiées ou de liens publicitaires.
*   **Sécurisation du Web :** Maintenir les systèmes WordPress et les plugins à jour pour éviter l'injection de scripts malveillants via des failles de plugins (ex: *Web Media Optimizer*).
*   **Surveillance réseau :** Surveiller les flux DNS suspects, notamment ceux utilisant le DoH vers des domaines inconnus, qui pourraient indiquer une activité de commande et de contrôle (C2).

---
[Source](https://thehackernews.com/2026/11/romulus-clickfix-attacks-deliver-rat.html){:target="_blank"}
