---
title: 'Phishing Campaign Hits 80+ Orgs Using SimpleHelp and ScreenConnect RMM Tools'
date: 2026-05-04
permalink: /posts/2026/05/04/phishing-campaign-hits-80-orgs-using-simplehelp-and-screenconnect-rmm-tools/
tags:
- veille-cyber
- hackernews
---
### Campagne de phishing "VENOMOUS#HELPER" : détournement d'outils RMM

Une campagne de phishing active, identifiée sous le nom de **VENOMOUS#HELPER** (ou STAC6405), cible plus de 80 organisations principalement aux États-Unis. L'objectif est d'établir un accès persistant via des outils d'administration à distance (RMM) légitimes, permettant aux attaquants de contourner les solutions de sécurité classiques.

**Points clés :**
* **Vecteur d'attaque :** Des emails de phishing usurpent l'identité de l'Administration de la Sécurité Sociale américaine (SSA).
* **Technique de contournement :** Utilisation de sites web légitimes compromis pour héberger des liens malveillants et contourner les filtres anti-spam.
* **Architecture redondante :** Les attaquants déploient simultanément **SimpleHelp** et **ScreenConnect**. Cette stratégie "dual-channel" garantit un accès permanent, même si l'un des outils est détecté et supprimé.
* **Persistance et furtivité :** L'outil SimpleHelp est installé en tant que service Windows avec une persistance en mode sans échec. Il intègre un mécanisme de "watchdog" pour redémarrer automatiquement et surveille en permanence la présence de logiciels de sécurité.
* **Élévation de privilèges :** Utilisation de l'exécutable légitime `elev_win.exe` pour obtenir des privilèges SYSTEM, permettant une prise de contrôle totale du poste (capture d'écran, injection de touches, transfert de fichiers).

**Vulnérabilités :**
Bien qu'il s'agisse de l'utilisation détournée de logiciels légitimes, cette campagne exploite l'absence de restrictions sur les outils de gestion à distance non autorisés par les politiques de sécurité (Shadow IT). Il n'y a pas de CVE spécifique exploitée ici, car l'attaque repose sur une installation volontaire par l'utilisateur (ingénierie sociale) et l'abus de fonctionnalités légitimes de SimpleHelp v5.0.1.

**Recommandations :**
* **Surveillance EDR/XDR :** Surveiller les comportements suspects liés aux outils RMM, notamment si leur installation n'est pas répertoriée dans le parc informatique de l'entreprise.
* **Contrôle des applications (AppLocker/WDAC) :** Restreindre l'exécution d'exécutables non autorisés, même ceux signés numériquement, lorsqu'ils ne sont pas nécessaires aux activités métiers.
* **Filtrage DNS et Web :** Bloquer les connexions sortantes vers les domaines de contrôle à distance non approuvés.
* **Sensibilisation :** Former les utilisateurs à la méfiance vis-à-vis des emails sollicitant le téléchargement de documents officiels via des liens externes.
* **Audit des services :** Rechercher les services Windows suspects possédant des capacités d'auto-redémarrage ou surveillant activement les processus de sécurité via WMI.

---
[Source](https://thehackernews.com/2026/05/phishing-campaign-hits-80-orgs-using.html){:target="_blank"}
