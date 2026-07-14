---
title: 'LabubaRAT Masquerades as NVIDIA Software to Control Windows Hosts'
date: 2026-07-14
permalink: /posts/2026/07/14/labubarat-masquerades-as-nvidia-software-to-control-windows-hosts/
tags:
- veille-cyber
- hackernews
---
### LabubaRAT : Une nouvelle menace modulaire dissimulée en logiciel NVIDIA

**Points clés :**
*   **Nature :** Découverte de LabubaRAT, un cheval de Troie d'accès à distance (RAT) développé en langage Rust.
*   **Stratégie :** Utilise le nom de fichier `nvidia-sysruntime.exe` pour se faire passer pour un composant logiciel NVIDIA et passer inaperçu.
*   **Modularité :** Le malware utilise une configuration dynamique transmise via des arguments en ligne de commande (souvent en Base64), permettant d'utiliser le même binaire pour différentes cibles sans serveurs de commande (C2) codés en dur.
*   **Persistance et flexibilité :** Supporte plusieurs protocoles de communication (HTTPS, WebView2, tunnel DNS) et propose un modèle potentiel de type "Malware-as-a-Service" (MaaS).
*   **Fonctionnalités :** Profilage complet du système (CPU, RAM, UAC), identification des logiciels de sécurité installés, exécution de commandes, capture d'écran, proxy SOCKS5 et transfert de fichiers.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'exécution malveillante d'un exécutable légitime usurpé et l'exploitation des privilèges utilisateur.

**Recommandations :**
*   **Surveillance réseau :** Bloquer ou surveiller les connexions vers le domaine associé `pipicka[.]xyz`.
*   **Analyse comportementale :** Surveiller les exécutions inhabituelles se faisant passer pour des composants NVIDIA, particulièrement ceux sollicitant des arguments suspects en ligne de commande ou tentant de lister des outils de sécurité.
*   **Gestion des accès :** Appliquer le principe du moindre privilège pour limiter l'impact en cas de compromission.
*   **Détection :** Configurer les solutions EDR/XDR pour détecter les outils de profilage système inhabituels et le trafic DNS anormal.

---
[Source](https://thehackernews.com/2026/07/labubarat-masquerades-as-nvidia.html){:target="_blank"}
