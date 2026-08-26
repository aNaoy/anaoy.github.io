---
title: 'Hackers abuse npm mirrors to host phishing redirect pages'
date: 2026-08-26
permalink: /posts/2026/08/26/hackers-abuse-npm-mirrors-to-host-phishing-redirect-pages/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement du registre npm pour l'hébergement de pages de phishing

Des acteurs malveillants exploitent le registre npm et ses plateformes de mise en miroir (comme UNPKG) pour héberger des pages HTML frauduleuses. Contrairement aux attaques classiques de chaîne d'approvisionnement, l'objectif n'est pas d'infecter les systèmes des développeurs, mais d'utiliser ces plateformes comme un espace de stockage gratuit, fiable et légitime pour diffuser des campagnes de phishing.

**Points clés :**
*   **Technique de détournement :** Des paquets npm minimaux contenant uniquement un fichier `index.html` sont publiés. Les miroirs npm permettent un accès direct à ces fichiers via un navigateur.
*   **Contournement de la sécurité :** En hébergeant les pages sur des domaines de confiance (ex: `unpkg.com`), les attaquants échappent aux filtres de sécurité qui bloquent habituellement leurs infrastructures malveillantes.
*   **Mécanisme de redirection :** Les pages imitent un CAPTCHA Cloudflare et exécutent un script JavaScript obfusqué pour rediriger l'utilisateur vers des sites de phishing.
*   **Persistance :** Les attaquants utilisent des services tiers (comme `api.keyval.org`) pour mettre à jour à distance les URL de redirection sans avoir à republier le paquet npm. De plus, les paquets supprimés du registre officiel peuvent rester accessibles sur les miroirs.

**Vulnérabilités :**
Il n'existe pas de CVE spécifique pour cette attaque, car il s'agit d'un abus de fonctionnalités légitimes de distribution de paquets (abus de confiance envers le domaine `unpkg.com` et le registre npm).

**Recommandations :**
*   **Surveillance :** Considérer toute requête HTTP directe vers des domaines de miroirs npm (tels qu'unpkg.com) comme potentiellement suspecte.
*   **Filtrage :** Renforcer les politiques de sécurité web pour bloquer ou inspecter les contenus provenant de miroirs de gestionnaires de paquets lorsqu'ils servent à afficher des pages HTML directement dans le navigateur.
*   **Vigilance :** Sensibiliser les utilisateurs à la méfiance envers les pages de vérification (CAPTCHA) redirigeant vers des sites tiers, même lorsqu'elles semblent hébergées sur des plateformes de confiance.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-abuse-npm-mirrors-to-host-phishing-redirect-pages/){:target="_blank"}
