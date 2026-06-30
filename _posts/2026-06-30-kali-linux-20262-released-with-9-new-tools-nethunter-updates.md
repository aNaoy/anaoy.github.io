---
title: 'Kali Linux 2026.2 released with 9 new tools, NetHunter updates'
date: 2026-06-30
permalink: /posts/2026/06/30/kali-linux-20262-released-with-9-new-tools-nethunter-updates/
tags:
- veille-cyber
- bleepingcomp
---
### Lancement de Kali Linux 2026.2 : Nouveaux outils et optimisations

La version 2026.2 de Kali Linux apporte des améliorations majeures en termes de performance et d'outillage pour les professionnels de la cybersécurité.

**Points clés :**
*   **Mise à jour noyau :** passage au noyau 6.19 (7.0 disponible en expérimental).
*   **Optimisation VM :** suppression du firmware graphique dans les images de machines virtuelles, réduisant la taille de l'initrd à 60 Mo et triplant la vitesse de démarrage.
*   **Environnements de bureau :** mise à jour vers GNOME 50 et KDE Plasma 6.6.
*   **Améliorations NetHunter :** support du flashage de noyau via Magisk, nouveaux pilotes d'injection (qcacld3) et corrections sur la fonctionnalité EvilTwin (Wi-Fi Fake AP).
*   **Nouveaux outils intégrés :** 9 outils ajoutés, notamment :
    *   *arsenal-ng* (librairie de cheat-sheets).
    *   *shell-gpt* (IA en ligne de commande).
    *   *legba* (bruteforcer multiprotocole).
    *   *oletools* (analyse de documents Office).
    *   *uro* (nettoyage d'URLs).
    *   *tookie-osint* (OSINT réseaux sociaux).
    *   *hydra-gtk*, *penelope* et *tailscale*.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée dans cette mise à jour de distribution ; il s'agit d'une mise à jour de maintenance et de fonctionnalités.

**Recommandations :**
*   **Mise à jour :** Pour les utilisateurs actuels, utilisez les commandes suivantes pour migrer vers la version 2026.2 :
    ```bash
    sudo apt update && sudo apt -y full-upgrade
    cp -vrbi /etc/skel/. ~/
    ```
*   **WSL :** Il est fortement conseillé aux utilisateurs du sous-système Windows pour Linux (WSL) d'utiliser WSL 2 pour une meilleure prise en charge des applications graphiques.
*   **Vérification :** Validez la mise à jour avec `grep VERSION /etc/os-release`.

---
[Source](https://www.bleepingcomputer.com/news/linux/kali-linux-20262-released-with-9-new-tools-nethunter-updates/){:target="_blank"}
