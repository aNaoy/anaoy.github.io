---
title: 'FortiBleed credential-theft campaign linked to Lynx ransomware'
date: 2026-07-02
permalink: /posts/2026/07/02/fortibleed-credential-theft-campaign-linked-to-lynx-ransomware/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne FortiBleed : Liens avec les ransomwares INC et Lynx

La campagne « FortiBleed » a permis le vol massif d'identifiants sur plus de 73 000 équipements Fortinet, compromettant potentiellement jusqu'à 430 000 pare-feu FortiGate à travers le monde. Des recherches récentes établissent un lien direct entre cette infrastructure de vol de données et les groupes de ransomware-as-a-service (RaaS) INC et Lynx (ce dernier étant suspecté d'être une nouvelle version d'INC).

**Points clés :**
* **Méthode d'attaque :** Utilisation d'un outil de capture de paquets (« FortiGate Sniffer ») pour intercepter les identifiants VPN et les données d'authentification directement dans le trafic réseau.
* **Infrastructure :** Environ 500 serveurs opérationnels ont été identifiés, ainsi qu'une équipe organisée d'environ 20 membres aux rôles définis.
* **Persistance :** Détection de comptes « backdoor » persistants sous le nom d'utilisateur `adminin` sur les systèmes compromis.
* **Échelle :** Initialement 19 000 dispositifs infectés par des renifleurs de trafic, chiffre ramené à environ 11 000 après notifications.

**Vulnérabilités :**
* Exploitation d'une vulnérabilité « zero-day » non divulguée dans Nextcloud pour étendre l'accès après une compromission initiale. Aucune CVE n'est associée à ce jour.

**Recommandations :**
* **Audit des comptes :** Rechercher et supprimer systématiquement tout compte utilisateur suspect ou inconnu, en particulier le compte `adminin`.
* **Réinitialisation :** Modifier immédiatement les identifiants VPN et les mots de passe d'administration sur l'ensemble des équipements FortiGate.
* **Analyse de trafic :** Surveiller les flux réseaux à la recherche de comportements anormaux typiques d'outils de capture de paquets.
* **Mise à jour :** Appliquer les correctifs de sécurité dès leur publication, notamment concernant les services périphériques comme Nextcloud.

---
[Source](https://www.bleepingcomputer.com/news/security/fortibleed-credential-theft-campaign-linked-to-lynx-ransomware/){:target="_blank"}
