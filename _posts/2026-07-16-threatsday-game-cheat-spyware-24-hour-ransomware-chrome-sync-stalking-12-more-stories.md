---
title: 'ThreatsDay: Game Cheat Spyware, 24-Hour Ransomware, Chrome Sync Stalking + 12 More Stories'
date: 2026-07-16
permalink: /posts/2026/07/16/threatsday-game-cheat-spyware-24-hour-ransomware-chrome-sync-stalking-12-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces cyber : Campagnes malveillantes et vulnérabilités critiques

Le paysage actuel des cybermenaces est marqué par une recrudescence de campagnes sophistiquées exploitant la confiance des utilisateurs, des logiciels légitimes et des vecteurs d'attaque classiques.

#### Points clés
*   **Prolifération des logiciels espions et RAT :** Des packages NuGet malveillants usurpant des outils de triche de jeux vidéo et des installateurs piégés (MobaXterm, Zoom) déploient des RAT (Starland, Remcos) pour le vol de données et de cryptomonnaies.
*   **Ransomware rapide :** Le nouveau ransomware "Spirals" a chiffré un réseau en moins de 24 heures après une compromission initiale via un web shell sur un serveur IIS.
*   **Abus de fonctionnalités légitimes :** Les "bind links" de Windows sont détournés pour contourner les solutions EDR (Endpoint Detection and Response). De plus, la synchronisation Chrome est détournée par des harceleurs pour espionner l'historique de navigation des victimes.
*   **Fraude financière à grande échelle :** Démantèlement de vastes réseaux de fraude à l'investissement (call centers, blanchiment via 800 comptes bancaires).
*   **Phishing évolué :** Usage de kits AI (Jalisco, OmegaLord) pour le détournement de jetons OAuth et le contournement du MFA, ainsi que des campagnes d'eCards piégées utilisant des outils RMM (Remote Monitoring and Management).

#### Vulnérabilités exploitées (CVE)
*   **CVE-2026-46817 :** Problème de gestion des privilèges dans Oracle E-Business Suite (critique).
*   **CVE-2023-4346 :** Mécanisme de verrouillage de compte défectueux dans le protocole KNX.
*   **CVE-2026-35273 :** Faille zero-day critique dans Oracle PeopleSoft exploitée par des groupes de cybercriminalité.

*Note : Les deux premières ont été ajoutées au catalogue KEV de la CISA en raison d'exploitations actives.*

#### Recommandations
*   **Validation rigoureuse :** Vérifier systématiquement l'authenticité des dépôts de code (GitHub, NuGet) et des installateurs logiciels. Ne pas accorder de confiance aveugle aux outils "utilitaires".
*   **Gestion des accès :** Désactiver les fonctionnalités de synchronisation non nécessaires, restreindre les privilèges administrateur (pour limiter les abus de `bindflt.sys`) et surveiller l'inscription de nouveaux appareils sur les comptes SaaS (Entra ID).
*   **Patching systématique :** Appliquer en priorité les correctifs pour les vulnérabilités listées dans le catalogue KEV de la CISA.
*   **Hygiène réseau :** Sécuriser les serveurs exposés (IIS) et surveiller les comportements anormaux post-intrusion pour stopper les attaques de ransomware dès les phases de reconnaissance.
*   **Transparence :** Adopter un cadre de divulgation coordonnée des vulnérabilités (CVD) pour renforcer la résilience des produits.

---
[Source](https://thehackernews.com/2026/07/threatsday-game-cheat-spyware-24-hour.html){:target="_blank"}
