---
title: 'Study of 281 Free Android VPN Apps Finds Traffic Leaks, Unencrypted Data, and Tracking'
date: 2026-07-10
permalink: /posts/2026/07/10/study-of-281-free-android-vpn-apps-finds-traffic-leaks-unencrypted-data-and-tracking/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques des VPN gratuits sur Android

Une étude approfondie menée par des chercheurs universitaires sur 281 applications VPN populaires du Google Play Store révèle des défaillances de sécurité majeures, exposant plus de 2,4 milliards d'installations à des risques accrus. L'outil d'audit utilisé, baptisé **MVPNalyzer**, a mis en évidence que ces applications échouent souvent à remplir leur fonction première : garantir la confidentialité.

**Points clés :**
*   **Fuites de données :** 29 applications présentent des fuites de trafic, incluant 24 applications qui exposent les requêtes DNS (révélant l'historique de navigation).
*   **Absence de chiffrement :** 4 applications n'utilisent aucun chiffrement pour le tunnel de données.
*   **Collecte de données abusives :** Plus de 80 % des applications contactent des serveurs publicitaires ou de suivi, collectant des identifiants publicitaires, des empreintes numériques de l'appareil (fingerprinting) et, dans certains cas, des coordonnées GPS.
*   **Défaut d'obfuscation :** 169 applications ne masquent pas leur trafic VPN, facilitant leur détection et leur blocage par les autorités ou les opérateurs réseau.
*   **Gestion défaillante :** Les labels "Verified" et les promesses "no-logs" du Play Store sont jugés davantage comme des outils marketing que comme des garanties réelles.

**Vulnérabilités identifiées :**
*   **Détournement de tunnel (Tunnel Hijacking) :** 5 applications téléchargent leurs fichiers de configuration en clair (HTTP), permettant à un attaquant sur le même réseau (ex: Wi-Fi public) de modifier la destination du trafic et de rediriger l'utilisateur vers un serveur malveillant.
*   **Chiffrement obsolète :** Utilisation de protocoles vulnérables, notamment Blowfish (**CVE-2016-6329**) et Triple DES (**CVE-2016-2183**), permettant de déchiffrer les communications capturées.
*   **Bibliothèques obsolètes :** Présence récurrente de versions de l'OpenSSL vulnérables à la faille **Heartbleed** (2014).

**Recommandations :**
*   **Prudence sur l'origine :** Privilégier des fournisseurs VPN reconnus qui publient régulièrement des audits de sécurité indépendants.
*   **Méfiance vis-à-vis du "Gratuit" :** Les applications gratuites financées par la publicité sont davantage susceptibles de collecter des données personnelles.
*   **Vérification :** Ne pas se fier uniquement aux labels "Verified" ou "Sécurisé" du Play Store ; consulter les listes d'audits indépendants pour vérifier si l'application utilisée est compromise.
*   **Transparence :** Favoriser les services transparents sur leur architecture technique et leur politique de gestion des données.

---
[Source](https://thehackernews.com/2026/07/study-of-281-free-android-vpn-apps.html){:target="_blank"}
