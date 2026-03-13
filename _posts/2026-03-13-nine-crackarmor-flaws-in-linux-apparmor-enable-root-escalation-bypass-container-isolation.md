---
title: 'Nine CrackArmor Flaws in Linux AppArmor Enable Root Escalation, Bypass Container Isolation'
date: 2026-03-13
permalink: /posts/2026/03/13/nine-crackarmor-flaws-in-linux-apparmor-enable-root-escalation-bypass-container-isolation/
tags:
- veille-cyber
- hackernews
---
### CrackArmor : Vulnérabilités critiques dans AppArmor

Le module de sécurité AppArmor du noyau Linux est touché par neuf vulnérabilités critiques, regroupées sous le nom « CrackArmor ». Présents depuis 2017, ces défauts de type « deputy confus » (confused deputy) permettent à un utilisateur non privilégié de manipuler les profils de sécurité, de contourner les restrictions d'isolation des conteneurs et d'exécuter du code arbitraire au niveau du noyau.

**Points clés :**
*   **Impact :** Élévation de privilèges vers le compte root, contournement de l'isolation des conteneurs et des restrictions d'espaces de noms (user namespaces).
*   **Conséquences :** Possibilité d'attaques par déni de service (DoS) via l'épuisement de la pile, fuite d'informations (KASLR), modification de fichiers sensibles (ex: `/etc/passwd`) et compromission de l'hôte.
*   **Portée :** Concerne tous les noyaux Linux depuis la version 4.11 utilisant AppArmor, soit des millions d'instances (Ubuntu, Debian, SUSE, etc.).
*   **Identifiants CVE :** Aucun identifiant n'a été attribué à ces vulnérabilités à ce jour.

**Recommandations :**
*   **Mise à jour immédiate :** L'installation des correctifs du noyau fournis par les distributeurs est la seule mesure de protection efficace.
*   **Priorisation :** Les environnements multi-utilisateurs et ceux utilisant des conteneurs doivent considérer le patching comme une priorité absolue, car les mesures d'atténuation temporaires ne garantissent pas un niveau de sécurité suffisant.

---
[Source](https://thehackernews.com/2026/03/nine-crackarmor-flaws-in-linux-apparmor.html){:target="_blank"}
