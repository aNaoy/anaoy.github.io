---
title: 'Researchers Push Over 2 Million Updates to Remotely Disable Popcorn Time Updater That Could Fuel a Botnet'
date: 2026-10-24
permalink: /posts/2026/10/24/researchers-push-over-2-million-updates-to-remotely-disable-popcorn-time-updater-that-could-fuel-a-botnet/
tags:
- veille-cyber
- hackernews
---
### Neutralisation préventive du botnet potentiel lié à Popcorn Time

Entre novembre 2025 et mars 2026, la société de cybersécurité Eye Security a mené l'« opération IXIM » pour désactiver à distance un service de mise à jour vulnérable présent sur le logiciel abandonné *Time4Popcorn*. Ce service, qui s'exécutait avec les privilèges les plus élevés (SYSTEM/root) et communiquait via des connexions non chiffrées, permettait potentiellement à n'importe quel acteur malveillant de prendre le contrôle de millions d'ordinateurs en détournant les noms de domaine expirés.

**Points clés :**
* **Envergure :** Plus de 2 millions de machines (Windows et Mac) ont reçu une mise à jour corrective déployée par Eye Security pour désactiver l'updater.
* **Risque :** Le logiciel utilisait des domaines non enregistrés pour chercher des mises à jour. En récupérant ces domaines, un attaquant aurait pu pousser du code malveillant (ransomware, vol de données, intégration à un botnet) directement sur les systèmes des utilisateurs.
* **Statut actuel :** La plupart des domaines critiques ont été transmis à la *Shadowserver Foundation*. Toutefois, certains domaines restent entre les mains de tiers, laissant les machines qui les interrogent potentiellement exposées.

**Vulnérabilité :**
* **CVE-2026-30612 :** Score de 9.8/10. Il s'agit d'une faille critique liée à l'absence de vérification d'authenticité et au manque de chiffrement du mécanisme de mise à jour automatique.
* **Versions affectées :** Windows (jusqu'à 6.2.1.18), Mac (jusqu'à 6.2.1.17) et Android (jusqu'à 3.5.0.173).

**Recommandations :**
* **Action prioritaire :** Désinstaller complètement *Popcorn Time*, car l'application elle-même reste dangereuse (moteur de navigateur obsolète, *sandbox* désactivée, vulnérabilités supplémentaires).
* **Désactivation manuelle (pour les utilisateurs avancés) :**
    * **Windows :** Exécuter `sc.exe stop "Update service"` puis `sc.exe config "Update service" start= disabled` dans un terminal.
    * **Mac :** Exécuter `launchctl unload -w /Library/LaunchDaemons/PT.updd.plist`.
* **Pour les administrateurs réseau :** Rechercher les fichiers `Updater.exe` (Windows) et `PT.updd` (Mac) et surveiller les requêtes réseau vers les domaines identifiés dans le rapport technique d'Eye Security.

---
[Source](https://thehackernews.com/2026/10/researchers-push-over-2-million-updates.html){:target="_blank"}
