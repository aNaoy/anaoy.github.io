---
title: 'Chrome Extension Caught Injecting Hidden Solana Transfer Fees Into Raydium Swaps'
date: 2025-11-26
permalink: /posts/2025/11/26/chrome-extension-caught-injecting-hidden-solana-transfer-fees-into-raydium-swaps/
tags:
- veille-cyber
- hackernews
---
### Extension Chrome Malveillante Vole des Fonds Solana

Une extension du Chrome Web Store nommée "Crypto Copilot" a été découverte en train d'injecter des frais de transfert cachés lors des échanges sur la plateforme Raydium, une bourse décentralisée sur la blockchain Solana. L'extension, qui se présente comme un outil d'aide au trading, insère secrètement une transaction de transfert de Solana vers un portefeuille contrôlé par l'attaquant.

**Points Clés :**

*   **Fonctionnalité Malveillante :** L'extension ajoute un `SystemProgram.transfer` non divulgué à chaque transaction d'échange Solana effectuée par l'utilisateur.
*   **Transfert de Fonds :** Les fonds détournés sont envoyés vers un portefeuille pré-codé dans l'extension.
*   **Calcul des Frais :** Les frais détournés correspondent à un minimum de 0.0013 SOL pour les petits échanges, et à 2.6 SOL plus 0.05% du montant échangé pour les transactions plus importantes.
*   **Dissimulation :** Des techniques comme la minification et le renommage de variables sont utilisées pour masquer le code malveillant.
*   **Infrastructure :** L'extension communique avec des serveurs externes pour enregistrer les portefeuilles, récupérer des données et signaler l'activité des utilisateurs. Les domaines associés ne proposent pas de produit légitime.
*   **Apparence Légitime :** L'extension utilise des services réels comme DexScreener et Helius RPC pour paraître digne de confiance.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifiques associées à cette extension. La vulnérabilité réside dans la conception et la distribution de l'extension elle-même.

**Recommandations :**

*   Les utilisateurs doivent être extrêmement prudents quant aux extensions de navigateur qu'ils installent, en particulier celles liées aux cryptomonnaies.
*   Il est conseillé de vérifier attentivement les autorisations demandées par les extensions et de lire les avis des autres utilisateurs.
*   Inspecter systématiquement les détails de chaque transaction avant de la signer, surtout lorsque l'on utilise des outils tiers.
*   Privilégier les plateformes et outils dont la réputation est solidement établie et vérifiée.
*   En cas de doute, supprimer immédiatement l'extension suspecte.

---
[Source](https://thehackernews.com/2025/11/chrome-extension-caught-injecting.html){:target="_blank"}
