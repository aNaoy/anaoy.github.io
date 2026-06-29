---
title: 'Adding some Automation to the favicon.ico method of Host Recon, (Mon, Jun 29th)'
date: 2026-06-29
permalink: /posts/2026/06/29/adding-some-automation-to-the-faviconico-method-of-host-recon-mon-jun-29th/
tags:
- veille-cyber
- sans-isc
---
### Automatisation de la reconnaissance d'hôtes via l'empreinte Favicon

L'utilisation du fichier `favicon.ico` est une technique efficace pour identifier des actifs appartenant à une même entité. Comme de nombreuses organisations déploient systématiquement la même icône sur leurs serveurs, il est possible de retrouver des hôtes isolés ou oubliés en indexant le hash de ce fichier via des moteurs de recherche comme Shodan.

**Points clés :**
*   **Empreinte (Fingerprinting) :** Le calcul du hash MurmurHash3 d'un `favicon.ico` permet d'identifier de manière unique une icône à travers le web.
*   **Automatisation :** Le processus consiste à extraire le hash d'une cible connue, à interroger l'API de Shodan pour trouver les hôtes partageant ce hash, puis à traiter les données JSON obtenues (via `jq`) pour extraire une liste propre de noms d'hôtes.
*   **Exploitation :** Une fois la liste des noms d'hôtes consolidée, celle-ci peut être utilisée pour des scans de découverte (Nmap) et d'énumération de ports à grande échelle (Masscan).

**Vulnérabilités associées :**
*   Cette technique ne s'appuie pas sur une CVE spécifique, mais exploite une **faiblesse de configuration (reconnaissance de surface d'attaque)**. L'exposition d'identifiants uniques (favicon identique) sur des infrastructures disparates facilite le regroupement d'actifs par un attaquant, augmentant ainsi la surface d'exposition.

**Recommandations :**
*   **Isolation des actifs :** Éviter de partager les mêmes fichiers statiques (favicons, CSS, scripts) sur des serveurs exposant des services critiques et des serveurs de développement ou de test.
*   **Réduction de la surface d'attaque :** Surveiller les actifs exposés sur Internet et supprimer les services ou hôtes obsolètes qui pourraient être indexés par des moteurs comme Shodan.
*   **Validation des résultats :** Toujours vérifier manuellement les découvertes automatisées, car cette méthode peut générer des faux positifs (services mutualisés ou CDN utilisant des icônes par défaut).

---
[Source](https://isc.sans.edu/diary/rss/33110){:target="_blank"}
