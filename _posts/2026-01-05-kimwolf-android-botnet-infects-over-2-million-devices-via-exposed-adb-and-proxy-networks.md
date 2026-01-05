---
title: 'Kimwolf Android Botnet Infects Over 2 Million Devices via Exposed ADB and Proxy Networks'
date: 2026-01-05
permalink: /posts/2026/01/05/kimwolf-android-botnet-infects-over-2-million-devices-via-exposed-adb-and-proxy-networks/
tags:
- veille-cyber
- hackernews
---
**Kimwolf : Le Botnet Android qui Exploite les Proxies Résidentiels**

Un botnet Android nommé Kimwolf a compromis plus de 2 millions d'appareils en exploitant des réseaux de proxies résidentiels. Les acteurs malveillants monétisent ce botnet par le biais d'installations d'applications, de la vente de bande passante proxy et de la fourniture de fonctionnalités DDoS.

Kimwolf, une variante Android du botnet AISURU, est suspecté d'être à l'origine d'attaques DDoS d'envergure. Le malware transforme les appareils infectés en relais pour du trafic malveillant et des attaques par déni de service distribué. La majorité des infections se concentrent au Vietnam, au Brésil, en Inde et en Arabie Saoudite.

Les attaques ciblent principalement les appareils Android disposant d'un service Android Debug Bridge (ADB) exposé. Une part significative de ces appareils n'est pas authentifiée et possède ADB activé par défaut, souvent pré-infectée par des kits de développement logiciel (SDK) de fournisseurs de proxy. Les appareils les plus touchés incluent des téléviseurs intelligents et des boîtiers décodeurs non officiels fonctionnant sous Android.

Le botnet a également exploité des adresses IP proxy louées par des fournisseurs basés en Chine, bien que certains aient depuis implémenté des correctifs de sécurité pour bloquer les accès non autorisés. Le modus operandi consiste à passer par des réseaux de proxies pour déployer le malware sur les appareils cibles.

**Points Clés :**

*   **Infections massives :** Plus de 2 millions d'appareils Android compromis.
*   **Méthode d'infection :** Exploitation de l'Android Debug Bridge (ADB) exposé et des réseaux de proxies résidentiels.
*   **Monétisation :** Vente de bande passante proxy, installations d'applications, et fourniture de capacités DDoS.
*   **Impact potentiel :** Implication dans des attaques DDoS record et des attaques par bourrage d'identifiants.
*   **Appareils ciblés :** Principalement des appareils Android avec ADB non sécurisé, y compris des Smart TVs et des set-top boxes non officiels.

**Vulnérabilités :**

*   **ADB (Android Debug Bridge) exposé et non authentifié :** Permet un accès non autorisé aux appareils Android. Aucune CVE spécifique n'est mentionnée dans l'article pour cette faille générale, mais il s'agit d'une mauvaise configuration courante.

**Recommandations :**

*   **Pour les fournisseurs de proxies :** Bloquer les requêtes vers les adresses IP privées (RFC 1918) pour empêcher l'exploitation des réseaux locaux.
*   **Pour les organisations :** Sécuriser les appareils exécutant des shells ADB non authentifiés afin d'empêcher tout accès non autorisé.

---
[Source](https://thehackernews.com/2026/01/kimwolf-android-botnet-infects-over-2.html){:target="_blank"}
