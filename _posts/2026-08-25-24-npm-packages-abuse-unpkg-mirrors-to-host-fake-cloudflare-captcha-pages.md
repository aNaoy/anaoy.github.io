---
title: '24 npm Packages Abuse unpkg Mirrors to Host Fake Cloudflare CAPTCHA Pages'
date: 2026-08-25
permalink: /posts/2026/08/25/24-npm-packages-abuse-unpkg-mirrors-to-host-fake-cloudflare-captcha-pages/
tags:
- veille-cyber
- hackernews
---
### Abus de l’infrastructure npm pour l’hébergement de campagnes de phishing

Une campagne malveillante utilise 24 paquets npm pour détourner des services de mise en miroir (notamment unpkg) et héberger des pages de faux CAPTCHA Cloudflare. L'objectif n'est pas d'infecter les développeurs qui installent ces paquets, mais d'exploiter la réputation et la persistance des registres npm pour stocker des charges utiles de phishing.

**Points clés :**
*   **Technique de détournement :** Les attaquants publient des paquets npm contenant un simple fichier HTML. Une fois indexé par des services comme `unpkg.com`, le fichier devient une page web légitime aux yeux des filtres de sécurité, facilitant l'accès aux victimes.
*   **Mécanisme « ClickFix » :** La page affiche un faux test de vérification Cloudflare. Une interaction de l'utilisateur déclenche un script JavaScript qui redirige vers des domaines malveillants.
*   **Utilisation de services légitimes comme relais :** Pour contourner les listes de blocage (comme Google Safe Browsing), les attaquants utilisent le service de stockage public `KeyVal` comme un « dead drop resolver » pour dynamiser et masquer les URL de redirection finale.
*   **Persistance :** Les paquets présents sur les miroirs npm peuvent rester accessibles indéfiniment, même après leur suppression du registre officiel.

**Vulnérabilités :**
Il ne s'agit pas de vulnérabilités logicielles classiques (CVE), mais d'un abus de confiance envers les CDN et les registres de paquets (Supply Chain Abuse). Aucune CVE n'a été attribuée à cette campagne, car elle repose sur l'exploitation détournée de fonctionnalités légitimes d'hébergement.

**Recommandations :**
*   **Vigilance accrue :** Ne pas se fier aveuglément à la réputation d'un domaine (comme `unpkg.com`) pour valider la légitimité d'un contenu.
*   **Analyse des liens :** Se méfier des tests CAPTCHA inattendus, particulièrement s'ils apparaissent sur des sites tiers ou après avoir cliqué sur des liens suspects.
*   **Surveillance de la chaîne d'approvisionnement :** Les organisations doivent surveiller les dépendances npm suspectes ou inconnues intégrées dans leurs projets, bien que le risque ici soit davantage tourné vers l'utilisateur final que vers l'intégrité du code source.
*   **Blocage par filtrage :** Envisager de limiter l'accès aux services de stockage de clés publics si leur usage n'est pas justifié dans un environnement professionnel, afin d'entraver les techniques de « dead drop ».

---
[Source](https://thehackernews.com/2026/08/24-npm-packages-abuse-unpkg-mirrors-to.html){:target="_blank"}
