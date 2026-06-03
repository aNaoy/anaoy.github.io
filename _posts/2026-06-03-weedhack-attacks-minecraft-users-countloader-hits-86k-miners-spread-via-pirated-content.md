---
title: 'Weedhack Attacks Minecraft Users, CountLoader Hits 86K, Miners Spread via Pirated Content'
date: 2026-06-03
permalink: /posts/2026/06/03/weedhack-attacks-minecraft-users-countloader-hits-86k-miners-spread-via-pirated-content/
tags:
- veille-cyber
- hackernews
---
### Menaces émergentes : Malware-as-a-Service, loaders et mineurs malveillants

Plusieurs campagnes de cybercriminalité exploitent actuellement des contenus populaires (Minecraft, logiciels piratés, streaming illégal) pour compromettre des systèmes à grande échelle.

**Points clés :**
*   **Weedhack (Minecraft) :** Une plateforme de type *Malware-as-a-Service* (MaaS) ciblant les joueurs de Minecraft via YouTube et le SEO. Elle propose des versions gratuites et payantes (dès 4,99 $) permettant l'exfiltration de données, le vol de jetons de session et l'accès à distance (webcam, keylogger).
*   **CountLoader :** Un chargeur JavaScript responsable de l'infection de 86 000 machines. Il déploie des payloads variés (Cobalt Strike, infostealers) et se propage notamment via des clés USB.
*   **Cryptominage par piratage :** Des sites de streaming illégaux diffusent des mineurs de cryptomonnaies déguisés en mises à jour de lecteurs vidéo, utilisant le *DLL side-loading* pour s'exécuter.

**Vulnérabilités et vecteurs d'attaque :**
*   **Techniques d'injection :** Usage du *DLL side-loading* (exécution de code malveillant via des bibliothèques légitimes).
*   **Contournement de sécurité :** Désactivation proactive des exclusions de Windows Defender et manipulation des notifications UAC pour obtenir des privilèges élevés.
*   **Infrastructure C2 :** Utilisation de l'infrastructure blockchain (EtherHiding) pour masquer l'adresse des serveurs de commande et contrôle.
*   **Vecteurs d'infection :** SEO Poisoning, publicités YouTube, téléchargements de mods/clients Minecraft contrefaits, logiciels piratés et clés USB infectées.

*Note : Aucune CVE spécifique n'est mentionnée dans le rapport, les attaquants exploitant principalement des méthodes d'ingénierie sociale et de détournement de fonctionnalités système légitimes.*

**Recommandations :**
*   **Utilisation de sources officielles :** Ne télécharger des mods, jeux ou logiciels que depuis leurs plateformes officielles ou des dépôts vérifiés.
*   **Vigilance sur le contenu gratuit :** Se méfier des outils proposant des fonctionnalités "premium" gratuitement via des vidéos YouTube ou des liens tiers.
*   **Hygiène numérique :** Désactiver l'exécution automatique des périphériques USB et maintenir ses solutions de protection activement configurées sans créer d'exclusions suspectes.
*   **Conscience du risque :** Éviter les sites de streaming illégal ou de logiciels crackés, qui constituent des vecteurs d'infection majeurs pour les mineurs et RAT (Remote Access Trojans).

---
[Source](https://thehackernews.com/2026/06/weedhack-attacks-minecraft-users.html){:target="_blank"}
