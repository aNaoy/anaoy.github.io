---
title: 'Adobe Chrome extension flaw let sites access private WhatsApp chats'
date: 2026-07-22
permalink: /posts/2026/07/22/adobe-chrome-extension-flaw-let-sites-access-private-whatsapp-chats/
tags:
- veille-cyber
- bleepingcomp
---
### HermeticReader : Vulnérabilité critique dans l'extension Adobe Acrobat

L'extension Adobe Acrobat pour Google Chrome présentait une faille de sécurité majeure, baptisée **HermeticReader**, permettant à des sites web malveillants d'accéder aux conversations WhatsApp Web des utilisateurs sans aucune authentification.

**Points clés :**
*   **Mécanisme d'attaque :** En incitant une victime à visiter une page web piégée, un attaquant pouvait détourner le moteur « Hermes » utilisé par l'extension pour interagir avec WhatsApp.
*   **Exfiltration de données :** L'attaque permettait d'injecter du code dans le DOM de WhatsApp Web pour extraire les contacts, les noms de profil et l'intégralité des messages chargés à l'écran.
*   **Risque de détournement :** En manipulant le DOM, un attaquant pouvait également remplacer le QR code de connexion pour prendre le contrôle total du compte WhatsApp de la victime.
*   **Portée :** La vulnérabilité affectait environ 329 millions d'utilisateurs. Aucune preuve d'exploitation active n'a été constatée.

**Vulnérabilité :**
*   **CVE-2026-48294 :** Chaîne de vulnérabilités permettant une écriture non authentifiée dans le stockage interne de l'extension et une exécution de commandes arbitraires via l'injection d'une iframe malveillante.

**Recommandations :**
*   **Mise à jour immédiate :** Vérifiez que l'extension Adobe Acrobat pour Chrome est bien à jour. La version corrigée est la **26.5.2.3** (toute version égale ou inférieure à 26.5.2.1 est vulnérable).
*   **Gestion des extensions :** De manière générale, limitez le nombre d'extensions installées sur votre navigateur et examinez régulièrement les permissions accordées à celles-ci.

---
[Source](https://www.bleepingcomputer.com/news/security/adobe-chrome-extension-flaw-let-sites-access-private-whatsapp-chats/){:target="_blank"}
