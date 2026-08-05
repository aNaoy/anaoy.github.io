---
title: 'Trojanized npm Packages Employ NullReceiver Tactic to Decode C2 IP from Blockchain'
date: 2026-08-05
permalink: /posts/2026/08/05/trojanized-npm-packages-employ-nullreceiver-tactic-to-decode-c2-ip-from-blockchain/
tags:
- veille-cyber
- hackernews
---
### NullReceiver : L'évolution furtive du C2 via la Blockchain

Des chercheurs en cybersécurité ont identifié une nouvelle technique baptisée **NullReceiver**, utilisée par des groupes nord-coréens pour dissimuler l'adresse IP de leur serveur de commande et contrôle (C2). Cette méthode, qui succède à l'approche "EtherHiding", a été détectée dans deux paquets npm malveillants : `bianira-ui` et `fluid-type-ui`.

**Points clés :**
*   **Fonctionnement :** Au lieu d'utiliser des contrats intelligents ou des données de transaction (`calldata`), le malware consulte le portefeuille Ethereum de l'attaquant et lit l'adresse de destination de sa dernière transaction sortante.
*   **Encodage :** L'adresse IP du serveur C2 est encodée directement dans les octets de l'adresse de destination d'un transfert Ethereum sans valeur (zéro Ether) et sans données.
*   **Furtivité accrue :** Contrairement à EtherHiding, il n'y a pas de destination fixe ou de "charge utile" détectable par les outils de sécurité classiques. Chaque transaction utilise une adresse unique et jetable, rendant le suivi et l'attribution extrêmement difficiles.
*   **Optimisation :** L'absence de données dans les transactions réduit les coûts de "gaz" et élimine les champs exploitables pour la signature d'empreinte numérique par les systèmes de défense.

**Vulnérabilités :**
*   Il ne s'agit pas d'une faille logicielle classique (CVE), mais d'un détournement de la logique réseau. Les paquets npm concernés ont servi de vecteurs d'infection en permettant l'exécution du script malveillant sur les machines des victimes pour interroger la blockchain.

**Recommandations :**
*   **Surveillance des dépendances :** Auditer systématiquement les paquets open source ajoutés aux projets, surtout ceux provenant d'utilisateurs peu connus ou ayant un historique récent.
*   **Analyse du trafic réseau :** Mettre en place une surveillance rigoureuse des connexions sortantes vers des adresses IP suspectes ou non répertoriées, car le malware finit par contacter directement l'adresse IP extraite de la blockchain.
*   **Vigilance sur le recrutement :** Rester vigilant face aux campagnes d'ingénierie sociale (notamment sur LinkedIn via des offres d'emploi frauduleuses) qui incitent à télécharger ou exécuter des outils tiers infectés.

---
[Source](https://thehackernews.com/2026/08/trojanized-npm-packages-decode-c2-ip.html){:target="_blank"}
