---
title: 'New OVSwrap Linux Kernel Flaw Lets Local Users Gain Root via Open vSwitch'
date: 2026-08-05
permalink: /posts/2026/08/05/new-ovswrap-linux-kernel-flaw-lets-local-users-gain-root-via-open-vswitch/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique OVSwrap dans le noyau Linux : Élévation de privilèges via Open vSwitch

Une faille de corruption de mémoire dans le datapath du noyau Linux, baptisée **OVSwrap**, permet à un utilisateur local non privilégié d'obtenir les privilèges root. Cette vulnérabilité, introduite par la suppression d'une limite de taille de données en mars 2025, affecte de nombreuses distributions Linux modernes configurées par défaut.

**Points clés :**
*   **Mécanisme :** L'exploitation repose sur un dépassement d'entier (wrap-around) dans le champ de longueur des attributs Netlink lors du traitement des actions Open vSwitch (OVS). 
*   **Accessibilité :** Aucun privilège particulier n'est requis au départ. Un utilisateur peut créer des espaces de noms (namespaces) réseau, charger automatiquement le module `openvswitch` et déclencher l'exploitation.
*   **Fiabilité :** Le chercheur Asim Manizada qualifie la faille de "fiable" et propose un exploit fonctionnel prenant en charge environ 800 versions de noyaux.
*   **Impact :** L'exploit permet de lire la mémoire du noyau, de corrompre des identifiants (credentials) et d'obtenir un shell root, transformant une compromission d'un compte utilisateur isolé en un accès total au serveur.

**Vulnérabilité :**
*   **CVE-2026-64531** (Score CVSS : 7.8)

**Recommandations :**
*   **Mise à jour :** Appliquer les correctifs du noyau fournis par votre distribution (le correctif amont est disponible depuis le 24 juillet 2026).
*   **Blocage du module :** Si Open vSwitch n'est pas nécessaire, désactivez le chargement du module en créant le fichier `/etc/modprobe.d/ovswrap.conf` contenant la ligne : `install openvswitch /bin/false`.
*   **Nettoyage :** Si le module est déjà chargé en mémoire, déchargez-le manuellement (`rmmod`) ou redémarrez le système.
*   **Sécurisation :** La désactivation des espaces de noms utilisateur non privilégiés peut limiter la surface d'attaque, bien que cela ne bloque pas les conteneurs disposant déjà de `CAP_NET_ADMIN`.

---
[Source](https://thehackernews.com/2026/08/new-ovswrap-linux-kernel-flaw-lets.html){:target="_blank"}
