---
title: 'Attackers Hijacked Over 300 Tor Exit Relays to Intercept SSH Connections'
date: 2026-10-21
permalink: /posts/2026/10/21/attackers-hijacked-over-300-tor-exit-relays-to-intercept-ssh-connections/
tags:
- veille-cyber
- hackernews
---
### Compromission massive de nœuds de sortie Tor pour l'interception de connexions SSH

Début octobre 2026, plus de 300 nœuds de sortie Tor ont été détournés pour intercepter des connexions SSH. Les attaquants ont modifié les fichiers de configuration (`torrc`) des serveurs compromis pour rediriger le trafic SSH vers des serveurs malveillants, permettant ainsi le vol de mots de passe saisis par les utilisateurs.

**Points clés :**
* **Méthode :** Les attaquants ont pris le contrôle de serveurs Linux hébergeant des relais Tor, souvent via le malware **Ebury** (une porte dérobée persistante pour OpenSSH).
* **Vecteur d'attaque :** Une fois le contrôle root obtenu, les attaquants ont modifié la politique de sortie du nœud pour autoriser le port 22 et rediriger le trafic vers 12 serveurs d'interception.
* **Impact :** Les utilisateurs se connectant via ces nœuds étaient confrontés à une usurpation de clé d'hôte SSH. Si l'utilisateur acceptait la fausse clé et saisissait son mot de passe, celui-ci était dérobé. 
* **Limitation :** Seules les authentifications par mot de passe étaient vulnérables ; l'authentification par clé SSH est restée sécurisée car le protocole nécessite une signature cryptographique spécifique à la session.
* **Résolution :** Le projet Tor a identifié et exclu les relais malveillants du réseau entre le 4 et le 5 octobre 2026.

**Vulnérabilités :**
* Le risque principal provient de l'utilisation du malware **Ebury** (version 1.8.3 identifiée), qui permet une persistance au niveau root et l'exfiltration de données sans laisser de traces classiques.
* Mauvaise hygiène de sécurité : réutilisation de mots de passe, stockage de mots de passe en clair sur les serveurs et authentification par mot de passe SSH activée sur des machines exposées.

**Recommandations pour les opérateurs de relais :**
* **Vérification :** Inspecter les fichiers `torrc`, les règles NAT (port 22), les processus suspects et la présence du fichier `libkeyutils.so.1.10.2` (setuid).
* **Audit :** Utiliser les scripts de détection ESET mis à jour pour identifier la présence d'Ebury.
* **Réponse :** En cas de compromission, ne pas tenter de nettoyer le serveur : le mettre hors ligne, conserver les preuves, réinstaller le système à partir de zéro, générer de nouvelles identités de relais et renouveler tous les identifiants/clés ayant transité sur la machine.
* **Bonnes pratiques :** Privilégier l'authentification par clé SSH, désactiver l'authentification par mot de passe pour le compte root, et isoler les environnements de gestion.

---
[Source](https://thehackernews.com/2026/10/attackers-hijacked-over-300-tor-exit.html){:target="_blank"}
