---
title: 'Japanese energy firm loses drive with data of 10.9 million clients'
date: 2026-06-12
permalink: /posts/2026/06/12/japanese-energy-firm-loses-drive-with-data-of-109-million-clients/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données massive chez Kyushu Electric Power

La compagnie d'électricité japonaise Kyushu Electric Power a annoncé la perte d'un support de stockage externe contenant les informations personnelles de 10,9 millions de clients. Le disque, utilisé pour une opération de sauvegarde le 27 avril, a disparu d'un cabinet sécurisé d'une salle des serveurs, constaté manquant le 26 mai. Une enquête interne ainsi qu'une plainte auprès de la police ont été déposées, sans succès à ce jour.

**Points clés :**
* **Impact :** 10,9 millions de comptes clients concernés dans la région de Kyushu.
* **Données exposées :** Noms, adresses de service, données de consommation électrique, numéros de téléphone et noms des fournisseurs de détail.
* **Absence de données bancaires :** Les informations de paiement (comptes bancaires, cartes de crédit) ne figuraient pas sur le support.
* **Contexte :** 57 employés avaient accès à la zone sécurisée. Les autorités japonaises (METI) ont exigé un rapport complet et des mesures correctives d'ici le 8 juillet.

**Vulnérabilités :**
* Aucune vulnérabilité logicielle (CVE) n'est associée, il s'agit d'une défaillance grave en **sécurité physique**.
* Défaut de contrôle d'accès : laisser une armoire contenant des données sensibles déverrouillée dans une zone à accès restreint.
* Absence de chiffrement : les données sur le disque externe n'étaient visiblement pas chiffrées, rendant les informations immédiatement lisibles en cas de vol ou de perte.

**Recommandations :**
* **Chiffrement systématique :** Appliquer un chiffrement fort sur tout support de stockage amovible contenant des données sensibles (données au repos).
* **Gestion des accès physiques :** Renforcer la surveillance des salles serveurs (vidéosurveillance, journaux d'accès électronique) et instaurer une politique stricte de verrouillage des armoires.
* **Politique de sauvegarde :** Privilégier des solutions de sauvegarde réseau sécurisées ou cloud plutôt que des supports physiques transportables.
* **Audit et inventaire :** Mettre en place un processus de traçabilité strict pour le suivi des supports amovibles (registre d'entrée/sortie).

---
[Source](https://www.bleepingcomputer.com/news/security/japanese-energy-firm-loses-drive-with-data-of-109-million-clients/){:target="_blank"}
