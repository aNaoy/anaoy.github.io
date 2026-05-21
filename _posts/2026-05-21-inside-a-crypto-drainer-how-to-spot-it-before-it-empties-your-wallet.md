---
title: 'Inside a Crypto Drainer: How to Spot it Before it Empties Your Wallet'
date: 2026-05-21
permalink: /posts/2026/05/21/inside-a-crypto-drainer-how-to-spot-it-before-it-empties-your-wallet/
tags:
- veille-cyber
- bleepingcomp
---
### L'essor du "Drainer-as-a-Service" : Menaces sur les portefeuilles crypto

Le paysage de la cybercriminalité a évolué vers des plateformes structurées de "Drainer-as-a-Service" (DaaS), à l'instar de *Lucifer*. Ces organisations fonctionnent comme de véritables entreprises SaaS, offrant aux affiliés des outils automatisés pour dérober des actifs cryptographiques via l'ingénierie sociale plutôt que par le piratage technique des appareils.

**Points clés :**
*   **Modèle économique :** Les développeurs maintiennent l'infrastructure (signature, exécution du vol) et prélèvent une commission (souvent 20 %) sur chaque "hit". Les affiliés se chargent de générer le trafic via du phishing.
*   **Professionnalisation :** Les services DaaS proposent désormais le clonage de sites, des systèmes de déploiement automatisés ("Zero Config") et un support client.
*   **Résilience :** En cas de suppression de leurs infrastructures (bots Telegram, domaines), ces groupes migrent rapidement vers des solutions décentralisées comme l'IPFS pour assurer la pérennité de leurs opérations.
*   **Techniques d'attaque :** Utilisation intensive des fonctions `Permit` et `Permit2` pour obtenir des autorisations de transfert de jetons sans que la victime ne réalise l'ampleur de la transaction.

**Vulnérabilités exploitées :**
Il n'existe pas de CVE spécifique, car il s'agit d'abus de fonctionnalités légitimes :
*   **Permit / Permit2 :** Mécanismes de signature hors chaîne permettant des transferts d'actifs avec une autorisation préalable de la victime.
*   **Gestion des permissions Web3 :** Complexité des requêtes de signature que l'utilisateur moyen peine à interpréter.

**Recommandations pour la sécurité :**
*   **Méfiance systématique :** Être vigilant face aux demandes de connexion immédiate à un portefeuille, aux offres "d'airdrop" ou aux mints d'NFT suspects, surtout s'ils proviennent de messageries privées (Discord, Telegram).
*   **Analyse des transactions :** Ne jamais signer une transaction ou une autorisation sans comprendre exactement ce qu'elle permet (vérifier si elle concerne l'accès illimité à vos jetons via `Permit`).
*   **Hygiène numérique :** Utiliser des portefeuilles distincts pour les interactions Web3 et ne pas utiliser son portefeuille principal (contenant la majorité des fonds) sur des sites inconnus ou non vérifiés.
*   **Vérification :** Ignorer les pressions liées à l'urgence (ex: "offre limitée") et privilégier l'usage de plateformes reconnues plutôt que des sites clonés.

---
[Source](https://www.bleepingcomputer.com/news/security/inside-a-crypto-drainer-how-to-spot-it-before-it-empties-your-wallet/){:target="_blank"}
