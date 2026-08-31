---
title: 'ValleyRAT Backdoor Hides in Signed Adware That Users Add to Antivirus Exclusions'
date: 2026-08-31
permalink: /posts/2026/08/31/valleyrat-backdoor-hides-in-signed-adware-that-users-add-to-antivirus-exclusions/
tags:
- veille-cyber
- hackernews
---
### Infiltration par ValleyRAT via des logiciels publicitaires signés

Le groupe de cybercriminels « Silver Fox » déploie le backdoor **ValleyRAT** (alias Winos 4.0) en utilisant une version modifiée de l'outil de fond d'écran légitime « QN Wallpaper ». Cette campagne exploite la confiance des utilisateurs qui ajoutent ce logiciel publicitaire à leurs listes d'exclusion antivirus.

**Points clés :**
*   **Technique d'exécution :** Le malware utilise le *DLL sideloading*. L'exécutable signé `QnWallpaper.exe` charge une bibliothèque malveillante `libcef.dll`, permettant au code malveillant de s'exécuter sous un processus légitime et signé.
*   **Neutralisation des défenses :** L'installateur désactive Windows Defender via la clé de registre `DisableAntiSpyware` et s'octroie des droits administrateur via `runas` si nécessaire.
*   **Persistance et protection :** Le malware s'ajoute aux entrées de démarrage automatique et se marque comme « processus critique » pour provoquer un écran bleu (BSOD) en cas de tentative d'arrêt forcé.
*   **Capacités malveillantes :** ValleyRAT permet un contrôle total de la machine, incluant le vol de frappes clavier, le contenu du presse-papiers, la capture d'écran et l'installation de modules supplémentaires.

**Vulnérabilités exploitées :**
*   **DLL Sideloading :** Exploitation de la confiance accordée aux fichiers signés par les systèmes de sécurité.
*   **Désactivation des protections :** Manipulation de la clé de registre `DisableAntiSpyware` (bien que non répertoriée comme une CVE spécifique, il s'agit d'une technique de contournement classique).
*   **Abus des exclusions AV :** La vulnérabilité réside principalement dans la pratique humaine d'exclure des logiciels suspects des analyses antivirus.

**Recommandations :**
*   **Gestion des exclusions :** Ne jamais ajouter de logiciels tiers ou d'utilitaires publicitaires aux listes d'exclusion des solutions de sécurité (EDR/Antivirus).
*   **Politiques de sécurité :** Appliquer des politiques strictes concernant l'installation de logiciels tiers sur les postes de travail.
*   **Hygiène logicielle :** Éviter l'utilisation d'applications à la réputation douteuse ou provenant de sources non fiables.
*   **Veille IoC :** Bloquer les connexions vers les adresses IP identifiées (`103.45.66.18`, `192.253.225.173`) et surveiller la présence du répertoire `C:\Program Files\QNWallpaper.4.0.1662\`.

---
[Source](https://thehackernews.com/2026/08/valleyrat-backdoor-hides-in-signed.html){:target="_blank"}
