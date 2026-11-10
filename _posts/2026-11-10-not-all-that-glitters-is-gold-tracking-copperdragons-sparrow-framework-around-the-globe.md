---
title: 'Not All That Glitters Is Gold: Tracking CopperDragon’s Sparrow Framework Around the Globe'
date: 2026-11-10
permalink: /posts/2026/11/10/not-all-that-glitters-is-gold-tracking-copperdragons-sparrow-framework-around-the-globe/
tags:
- veille-cyber
- zerodaysfans
---
### L'écosystème CopperDragon : Analyse du framework Sparrow

L'entité « CopperDragon » agit comme un fournisseur de services numériques pour plusieurs groupes de menace liés à la Chine. Elle distribue le framework modulaire **Sparrow**, une plateforme multiplateforme utilisée pour des opérations d'espionnage sophistiquées contre des télécommunications, des gouvernements et des infrastructures critiques en Amérique latine, en Asie et en Europe.

#### Points clés
*   **Structuration des attaques :** Trois clusters distincts ont été identifiés (SilentDelivery, OceanGate, DarkWire), chacun utilisant des vecteurs d'infection et des outils spécifiques.
*   **Polyvalence :** Le framework Sparrow supporte des variantes pour Windows et Linux, incluant des capacités de persistance, de mouvement latéral et de communication furtive.
*   **Évolution technique :** Les attaquants déploient des techniques avancées comme le *DLL sideloading*, des rootkits noyau (basés sur *Reptile*) et des backdoors passives interceptant le trafic via des drivers (ex: *WinDivert*).

#### Clusters d'activité
1.  **SilentDelivery (Europe/Asie) :** Utilise des attaques par *watering-hole* (sites compromis) injectant de faux avertissements de certificat SSL pour inciter au téléchargement de la backdoor **SquadC**.
2.  **OceanGate (Asie) :** Cible les infrastructures critiques. Exploite des serveurs Linux (via **SparrowShell** et **AnnobinDoor**) avant de migrer vers Windows pour déployer des outils de collecte de données et de vol d'identifiants (ex: **CopperLsa**).
3.  **DarkWire (Amérique latine) :** Se concentre sur les opérateurs télécoms. Utilise **CopperDoor** et **CopperDNS** (tunnellisation DNS) avec des outils de proxying pour maintenir un accès discret.

#### Vulnérabilités et vecteurs d'attaque
*   **Vecteurs d'infection :** Attaques par *watering-hole* (XSS sur sites tiers), hameçonnage ciblé (pièces jointes LNK) et exploitation de serveurs Linux exposés.
*   **Techniques de persistance :** Manipulation de clés de registre (*Run keys*), services système, et utilisation de rootkits noyau pour masquer processus et fichiers.
*   **Évasion :** Utilisation intensive de *DLL sideloading* (abusement de binaires légitimes), chiffrement personnalisé des payloads, et spoofing de la pile d'appels pour éviter la détection par les EDR.

#### Recommandations
*   **Surveillance réseau :** Surveiller les comportements anormaux liés au protocole DNS (requêtes MX suspectes) et restreindre les communications sortantes vers des IPs externes non autorisées.
*   **Gestion des privilèges :** Auditer les comptes locaux sur les machines Windows, particulièrement ceux ajoutés récemment au groupe Administrateurs, et désactiver les politiques de filtrage de jetons locaux (LocalAccountTokenFilterPolicy).
*   **Sécurisation Linux :** Renforcer la sécurité des serveurs exposés, monitorer les modifications sur les binaires systèmes (OpenSSH) et inspecter les modules noyau chargés (rootkits).
*   **Hygiène logicielle :** Bloquer les téléchargements de fichiers MSI ou exécutables provenant de sources non vérifiées suite à des erreurs de certificat "factices" dans les navigateurs.

---
[Source](https://research.checkpoint.com/2026/not-all-that-glitters-is-gold-tracking-copperdragons-sparrow-framework-around-the-globe/){:target="_blank"}
