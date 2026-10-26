---
title: 'uCreator Android Spyware Can Steal Telegram 2FA Passwords and Clone WeChat Accounts'
date: 2026-10-26
permalink: /posts/2026/10/26/ucreator-android-spyware-can-steal-telegram-2fa-passwords-and-clone-wechat-accounts/
tags:
- veille-cyber
- hackernews
---
### Menace uCreator : Espionnage Android et détournement de comptes

**uCreator** est un kit de logiciels espions Android sophistiqué, vendu comme un produit commercial, capable de compromettre des applications de messagerie populaires (Telegram, WeChat, etc.) via des copies altérées ou des conteneurs isolés (« Onion Box »).

**Points clés :**
* **Fonctionnement :** Le malware injecte du code malveillant dans des versions modifiées d'applications légitimes, fonctionnant avec les mêmes permissions que l'application originale.
* **Extraction de données :** Il intercepte les mots de passe de double authentification (2FA) en texte clair avant leur hachage, accède aux bases de données de messagerie et permet le clonage de comptes.
* **Discrétion :** Le malware peut masquer les sessions actives de l'attaquant sur l'appareil infecté, rendant le détournement invisible pour l'utilisateur.
* **Distribution :** Sideloading via des sites tiers, publicités intrusives et ingénierie sociale, particulièrement en Inde, au Brésil et en Indonésie.
* **Infrastructure :** Utilise un système de gestion centralisé (télécommandé via une console cloud) permettant aux clients d'effectuer des opérations de masse, comme l'ajout d'amis ou le vol d'identifiants, tout en simulant un comportement humain pour contourner les contrôles de sécurité.

**Vulnérabilités :**
Il n'existe pas de CVE spécifique exploitée, le malware repose sur une technique de **hooking** (interception d'appels système) pour manipuler le comportement des applications en mémoire. Le kit utilise des outils de patching type *LSPatch* et des techniques de virtualisation d'applications pour isoler et compromettre le trafic.

**Recommandations :**
* **Installation officielle :** Ne téléchargez et n'installez jamais d'applications en dehors des magasins officiels (Google Play Store).
* **Vérification des sources :** La signature numérique des fichiers APK est primordiale ; une application provenant d'un site tiers, même portant le nom d'un développeur connu, doit être systématiquement rejetée.
* **Hygiène numérique :** Méfiez-vous des applications de messagerie ou de chat proposées via des publicités contextuelles ou des sites de rencontres douteux.
* **Audit de sécurité :** Vérifiez régulièrement la liste des appareils connectés dans les paramètres de vos applications de messagerie. En cas de comportement anormal, révoquez immédiatement toutes les sessions actives et réinstallez l'application depuis une source officielle.

---
[Source](https://thehackernews.com/2026/10/ucreator-android-spyware-can-steal.html){:target="_blank"}
