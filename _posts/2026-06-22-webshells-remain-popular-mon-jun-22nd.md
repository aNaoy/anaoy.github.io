---
title: 'Webshells Remain Popular, (Mon, Jun 22nd)'
date: 2026-06-22
permalink: /posts/2026/06/22/webshells-remain-popular-mon-jun-22nd/
tags:
- veille-cyber
- sans-isc
---
### Persistance et évolution des webshells : Focus sur ZypeerShell

Les webshells PHP restent une menace persistante et active, comme en témoigne l'émergence récente de **ZypeerShell**, un outil présenté comme puissant et indétectable. Bien que ses fonctionnalités soient classiques, cet outil illustre la sophistication croissante des attaquants, notamment par l'usage d'obfuscation avancée et de techniques de post-exploitation.

**Points clés :**
*   **Fonctionnalités avancées :** ZypeerShell inclut des capacités de connexion vers des serveurs de commande et contrôle (C2) via GSocket, facilitant l'accès distant persistant.
*   **Obfuscation :** Le code est protégé par *Fortress Layer*, un chargeur multi-couches doté de contrôles d'intégrité pour entraver l'analyse statique.
*   **Dissimulation :** Certaines fonctions malveillantes (comme le déploiement de GSocket) sont présentes dans le code source mais ne sont pas appelées directement par l'interface graphique, une technique visant à échapper à la détection par simple inspection visuelle des menus.
*   **Distribution :** Le projet est promu sur GitHub et relayé au sein de canaux Telegram spécialisés, visant tant des acteurs malveillants que des équipes de test d'intrusion (red teaming).

**Vulnérabilités associées :**
*   L'utilisation d'un webshell repose sur l'exploitation préalable de vulnérabilités d'exécution de code à distance (RCE) ou de failles d'upload de fichiers sur les serveurs web ciblés. Bien que cet article ne cite pas de CVE spécifique, les vecteurs d'entrée classiques incluent les injections PHP non contrôlées ou les configurations serveurs permissives permettant l'exécution de scripts non autorisés.

**Recommandations :**
*   **Renforcement de la sécurité applicative :** Limiter strictement les droits d'écriture du serveur web sur les répertoires et désactiver l'exécution de scripts dans les dossiers de téléchargement de fichiers.
*   **Surveillance des logs :** Auditer régulièrement les accès aux répertoires web et surveiller les appels système inhabituels ou les connexions réseau sortantes vers des services non autorisés (comme GSocket).
*   **Analyse d'intégrité :** Utiliser des solutions de détection d'intrusion (HIDS) pour surveiller toute modification non autorisée des fichiers sources du site web.
*   **Gestion de la surface d'attaque :** Maintenir les applications PHP à jour et auditer régulièrement le code pour prévenir l'upload de fichiers malveillants.

---
[Source](https://isc.sans.edu/diary/rss/33096){:target="_blank"}
