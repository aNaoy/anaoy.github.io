---
title: 'Android 17 adds ECH support to make web browsing harder to track'
date: 2026-08-27
permalink: /posts/2026/08/27/android-17-adds-ech-support-to-make-web-browsing-harder-to-track/
tags:
- veille-cyber
- bleepingcomp
---
### Renforcement de la confidentialité réseau sur Android 17

Google déploie des mesures de sécurité réseau majeures dans Android 17 pour limiter le traçage des utilisateurs et renforcer la protection contre les interceptions malveillantes.

**Points clés**
*   **Support natif du protocole ECH (Encrypted Client Hello) :** Android 17 chiffre désormais la partie initiale de la négociation TLS. Cela empêche les fournisseurs d'accès (FAI) et les opérateurs Wi-Fi de voir les noms de domaines visités via le SNI (Server Name Indication).
*   **Protection du réseau local :** Les applications doivent désormais obtenir une autorisation explicite avant de scanner ou de se connecter aux appareils présents sur le réseau local de l'utilisateur.
*   **Transparence des certificats :** La transparence des certificats est activée par défaut, rendant la détection de certificats frauduleux plus rapide et fiable.
*   **Désactivation du 2G :** Les opérateurs partenaires peuvent désormais désactiver automatiquement la connectivité 2G, limitant les risques d'attaques par "SMS blasters" ou par de fausses antennes relais (rogue base stations).
*   **Mécanisme GREASE :** Pour éviter que les connexions ECH ne se distinguent, le système envoie des champs leurres lorsqu'un serveur ne supporte pas encore le protocole.

**Vulnérabilités adressées**
L'article ne mentionne pas de CVE spécifique, mais cible les failles suivantes :
*   **Fuite de métadonnées de navigation :** Exposition du nom de domaine via le SNI en clair.
*   **Attaques sur les réseaux mobiles hérités :** Vulnérabilités liées aux protocoles 2G obsolètes, propices aux interceptions de trafic et aux messages malveillants.
*   **Usurpation d'identité numérique :** Utilisation de certificats falsifiés pour des attaques de type Man-in-the-Middle.

**Recommandations**
*   **Pour les développeurs :** Mettre à jour les applications pour cibler Android 17 et utiliser des bibliothèques réseau compatibles (dernières versions de OkHttp, WebView ou HttpEngine) afin de bénéficier du chiffrement ECH.
*   **Pour les utilisateurs :** Privilégier l'utilisation d'Android 17 et vérifier que les options de protection réseau (DNS privé, désactivation 2G si disponible) sont actives pour limiter le profilage commercial et les interceptions par des tiers.

---
[Source](https://www.bleepingcomputer.com/news/security/android-17-adds-ech-support-to-make-web-browsing-harder-to-track/){:target="_blank"}
