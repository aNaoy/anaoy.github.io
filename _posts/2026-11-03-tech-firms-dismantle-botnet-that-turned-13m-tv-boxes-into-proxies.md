---
title: 'Tech Firms Dismantle Botnet That Turned 1.3M TV Boxes Into Proxies'
date: 2026-11-03
permalink: /posts/2026/11/03/tech-firms-dismantle-botnet-that-turned-13m-tv-boxes-into-proxies/
tags:
- veille-cyber
- krebs
---
### Démantèlement du botnet XCPE : quand les box TV deviennent des outils cybercriminels

Google, en collaboration avec divers partenaires de l'industrie, a démantelé le botnet « XCPE », qui contrôlait plus de 1,3 million de boîtiers Android TV. Ces appareils, fabriqués par la société chinoise Videostrong, étaient pré-équipés d'un logiciel malveillant dès leur sortie d'usine.

**Points clés :**
* **Modèle économique malveillant :** Le malware transformait les appareils en « proxys résidentiels », permettant à des tiers d'utiliser la connexion Internet des utilisateurs à leur insu pour anonymiser du trafic frauduleux, effectuer du scraping de données ou orchestrer des attaques DDoS.
* **Étendue de l'infection :** Au-delà des box TV, le malware XCPE a été détecté sur divers objets connectés (IoT) sous Android, incluant des équipements de télésanté, des machines de karaoké et des systèmes d'affichage numérique.
* **Implication des prestataires :** Plusieurs services de proxys résidentiels (comme AppSalt/Honeygain, NetNut, Grass, etc.) ont été identifiés comme bénéficiaires du trafic généré par ces appareils infectés.
* **Pratiques industrielles :** Des marques populaires, telles que MECOOL (fabriquées par Skyworth), ont été identifiées comme intégrant nativement ces composants malveillants, souvent promus via des influenceurs sur les réseaux sociaux.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais pointe une **vulnérabilité critique au niveau de la chaîne d'approvisionnement (supply chain attack)** : les fabricants installaient le malware au démarrage initial du système, contournant les protocoles de sécurité standards d'Android.

**Recommandations :**
* **Vigilance sur le matériel :** Privilégier des marques reconnues et certifiées pour leurs équipements connectés.
* **Mises à jour :** S'assurer que les systèmes d'exploitation des boîtiers multimédias sont maintenus à jour via les canaux officiels du fabricant.
* **Audit réseau :** Pour les utilisateurs avancés, surveiller le trafic sortant inhabituel provenant des objets connectés via des outils de filtrage réseau (DNS, pare-feu).
* **Référence technique :** Consulter la liste des modèles affectés publiée par *Synthient* (disponible sur leur GitHub) pour identifier si vos appareils figurent parmi les produits compromis.

---
[Source](https://krebsonsecurity.com/2026/11/tech-firms-dismantle-botnet-that-turned-1-3m-tv-boxes-into-proxies/){:target="_blank"}
