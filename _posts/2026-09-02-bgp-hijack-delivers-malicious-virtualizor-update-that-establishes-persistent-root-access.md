---
title: 'BGP Hijack Delivers Malicious Virtualizor Update That Establishes Persistent Root Access'
date: 2026-09-02
permalink: /posts/2026/09/02/bgp-hijack-delivers-malicious-virtualizor-update-that-establishes-persistent-root-access/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement Virtualizor par détournement BGP

Entre le 28 et le 30 août 2026, des attaquants ont utilisé un détournement de protocole BGP (*Border Gateway Protocol*) pour intercepter le trafic de mise à jour des services Virtualizor et Softaculous. En redirigeant les connexions vers un serveur malveillant muni d'un certificat Let's Encrypt valide, ils ont distribué une mise à jour compromise aux serveurs effectuant une vérification à ce moment-là.

**Points clés :**
* **Absence de signature cryptographique :** Le mécanisme de mise à jour ne vérifiant pas l'intégrité des paquets, les serveurs ont accepté le contenu malveillant sans alerte.
* **Persistance :** L'attaque installe un service *systemd*, ajoute une clé SSH non autorisée et crée un compte utilisateur (`proxyuser`) pour maintenir un accès root.
* **Portée :** Bien que l'incident ait touché un nombre limité de serveurs, aucune liste exhaustive des machines compromises n'est disponible.

**Vulnérabilités :**
* Absence de signature cryptographique des paquets de mise à jour.
* Vulnérabilité au détournement de routage (BGP Hijacking) permettant une attaque de type "Man-in-the-Middle".

**Recommandations :**
* **Pour les opérateurs :**
    * Exécuter immédiatement le [scanner officiel](https://files.virtualizor.com/security/virtualizor_security_scan.sh) fourni par Virtualizor.
    * Vérifier la présence du fichier `/etc/systemd/system/java-jre-update.service` et auditer les clés SSH, les utilisateurs et les tâches cron.
    * Restaurer les serveurs compromis via une réinstallation propre ("clean build").
    * Réinitialiser toutes les clés d'API et restreindre l'accès SSH aux adresses IP de confiance.
* **Pour les utilisateurs finaux :**
    * Réinitialiser les mots de passe de l'espace client (et ceux réutilisés ailleurs).
    * Surveiller les relevés bancaires en cas de saisie de données de paiement durant la période de l'incident.

---
[Source](https://thehackernews.com/2026/09/bgp-hijack-delivers-malicious.html){:target="_blank"}
