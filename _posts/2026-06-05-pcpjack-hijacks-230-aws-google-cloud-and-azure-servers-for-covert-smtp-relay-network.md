---
title: 'PCPJack Hijacks 230 AWS, Google Cloud, and Azure Servers for Covert SMTP Relay Network'
date: 2026-06-05
permalink: /posts/2026/06/05/pcpjack-hijacks-230-aws-google-cloud-and-azure-servers-for-covert-smtp-relay-network/
tags:
- veille-cyber
- hackernews
---
### PCPJack : Un réseau de relais SMTP clandestin basé sur des serveurs cloud compromis

Le groupe de cybercriminels **PCPJack** a détourné 230 serveurs cloud (AWS, Google Cloud et Azure) pour établir un réseau de relais SMTP destiné à des activités malveillantes massives, telles que le spam ou le phishing. Cette infrastructure opportuniste repose sur l'utilisation du framework **Sliver** et de l'outil de tunnelisation **Chisel**.

**Points clés :**
*   **Mode opératoire :** Les attaquants déploient des implants ("beacons") sur les serveurs compromis, qui sont ensuite convertis en proxys SOCKS5.
*   **Vérification automatisée :** Un script côté serveur (C2) teste en permanence la capacité des nœuds à relayer des emails vers `smtp.gmail.com:587`. Les hôtes inefficaces sont éliminés, tandis que les proxys fonctionnels sont synchronisés toutes les cinq minutes vers un serveur tiers.
*   **Persistance :** Les logiciels malveillants sont dissimulés sous forme de fichiers cachés (préfixés par un point) et persistés via `/var/tmp/.xs`.
*   **Découverte fortuite :** L'infrastructure a été exposée suite à une mauvaise configuration de sécurité : des répertoires contenant le code source, les scripts de déploiement et la configuration Sliver ont été laissés accessibles sans authentification sur le serveur C2 (`213.136.80.73`).

**Vulnérabilités :**
*   **Absence d'authentification :** Le serveur de commande et contrôle (C2) des attaquants présentait des répertoires ouverts, permettant l'exfiltration des outils de l'attaquant.
*   **Vecteur initial :** Bien que non spécifié comme une CVE unique, l'exploitation cible des serveurs cloud mal sécurisés par le vol d'identifiants. Les administrateurs doivent surveiller la présence de processus suspects comme les tunnels **Chisel** et les entrées persistantes (cron/systemd) pointant vers `/var/tmp/.xs`.

**Recommandations :**
*   **Audit des fichiers systèmes :** Rechercher la présence de fichiers cachés suspects dans `/var/tmp/` et vérifier les entrées de persistance (tâches cron, services systemd).
*   **Surveillance réseau :** Détecter les connexions sortantes inhabituelles vers des services SMTP externes provenant de serveurs ne nécessitant pas de capacités d'envoi d'emails.
*   **Durcissement (Hardening) :** Appliquer le principe du moindre privilège sur les serveurs cloud, restreindre les accès SSH/RDP et s'assurer que tous les accès aux outils de gestion d'infrastructure sont protégés par une authentification forte (MFA).
*   **Intégrité des processus :** Utiliser des outils de détection EDR pour repérer l'exécution de binaires Sliver ou Chisel, souvent utilisés pour maintenir des accès distants persistants.

---
[Source](https://thehackernews.com/2026/06/pcpjack-hijacks-230-aws-google-cloud.html){:target="_blank"}
