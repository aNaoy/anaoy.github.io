---
title: 'Over 100 Chrome Web Store extensions steal user accounts, data'
date: 2026-04-15
permalink: /posts/2026/04/15/over-100-chrome-web-store-extensions-steal-user-accounts-data/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de malwares massive sur le Chrome Web Store

Plus de 100 extensions malveillantes ont été identifiées sur le Chrome Web Store, opérant dans le cadre d'une campagne coordonnée de type "Malware-as-a-Service" (MaaS). Ces outils, déguisés en utilitaires, jeux ou extensions pour réseaux sociaux (Telegram, TikTok, YouTube), exploitent une infrastructure de commande et de contrôle (C2) centralisée pour exfiltrer des données sensibles et détourner des sessions utilisateur.

**Points clés :**
* **Détournement de sessions :** Les extensions ciblent particulièrement les sessions Telegram Web, permettant aux attaquants de remplacer les comptes des victimes par les leurs sans aucune interaction.
* **Vol d'identité Google :** Utilisation de l'API `chrome.identity.getAuthToken` pour récolter des profils utilisateurs et des jetons d'accès (OAuth2 Bearer tokens).
* **Backdoor persistante :** Installation de fonctions exécutées au démarrage du navigateur, permettant aux attaquants de commander l'ouverture d'URL arbitraires à distance.
* **Injection publicitaire :** Altération des en-têtes de sécurité et injection de publicités sur les plateformes de vidéo.

**Vulnérabilités :**
Aucune CVE spécifique n'est associée à cette campagne, car il s'agit d'un usage malveillant des fonctionnalités légitimes du navigateur via des autorisations accordées par l'utilisateur lors de l'installation (abus d'API). La menace repose sur l'exploitation de :
* `innerHTML` pour l'injection de code malveillant dans l'interface.
* `localStorage` pour le vol de jetons de session.
* Abus des autorisations `chrome.identity`.

**Recommandations :**
* **Audit immédiat :** Vérifier la liste des extensions installées dans Google Chrome et les comparer avec la liste des identifiants publiés dans le rapport de recherche de *Socket*.
* **Suppression :** Désinstaller sans délai toute extension suspecte identifiée comme faisant partie de cette campagne.
* **Principe de précaution :** Limiter l'installation d'extensions provenant d'éditeurs peu connus, même sur la boutique officielle, et révoquer les accès aux applications tierces suspectes dans les paramètres de sécurité des comptes Google et Telegram.

---
[Source](https://www.bleepingcomputer.com/news/security/over-100-chrome-extensions-in-web-store-target-users-accounts-and-data/){:target="_blank"}
