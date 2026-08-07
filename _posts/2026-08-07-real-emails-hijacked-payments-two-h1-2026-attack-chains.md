---
title: 'Real emails, hijacked payments: Two H1 2026 attack chains'
date: 2026-08-07
permalink: /posts/2026/08/07/real-emails-hijacked-payments-two-h1-2026-attack-chains/
tags:
- veille-cyber
- bleepingcomp
---
### Analyse des chaînes d'attaques exploitant la confiance : Rapport H1 2026

Le rapport de Gen Threat Labs met en lumière deux campagnes d'attaques majeures du premier semestre 2026. Plutôt que de pirater des systèmes sécurisés, les attaquants détournent des processus légitimes via des comptes compromis et des manipulations locales.

**Points clés :**
*   **Campagne de logiciels bancaires :** Utilisation de boîtes mail professionnelles légitimes pour envoyer des courriels piégés (factures, avis d'expédition). Le succès repose sur la confiance accordée à l'expéditeur. Une fois le document ouvert, une chaîne d'exécution (JavaScript, PowerShell, shellcode) installe des malwares (ex: GepyS, Remcos RAT, XWorm) qui modifient les paramètres proxy et ajoutent des extensions de navigateur malveillantes.
*   **Campagne de détournement de cryptomonnaies :** Utilisation d'un "clipper" compilé en Rust qui surveille le presse-papier de la victime. Lors d'une transaction, il remplace l'adresse du destinataire par une adresse contrôlée par l'attaquant. La communication avec le serveur de commande (C2) est dissimulée via des pointeurs stockés dans des smart contracts sur la Binance Smart Chain, rendant les blocages d'adresses IP classiques inefficaces.

**Vulnérabilités :**
*   **Absence de CVE spécifique :** Les attaques reposent sur l'exploitation de fonctionnalités légitimes ("Living off the Land") et sur le facteur humain (ingénierie sociale), et non sur des vulnérabilités logicielles identifiées avec des numéros CVE.
*   **Gestion des identités :** Compromission de comptes mail légitimes, contournant les filtres SPF/DKIM.
*   **Intégrité des données locales :** Le presse-papier est une zone non protégée permettant la substitution silencieuse de données sensibles (adresses de portefeuilles).

**Recommandations :**
*   **Analyse comportementale :** Ne pas se fier à la réputation de l'expéditeur. Corréler les événements (ouverture de pièce jointe -> lancement de script -> modification de proxy) comme une séquence unique et suspecte.
*   **Durcissement des postes :** Restreindre l'accès aux interpréteurs de scripts (PowerShell) pour les utilisateurs non techniques et appliquer des politiques de contrôle d'application strictes sur les pièces jointes téléchargées.
*   **Vérification des transactions crypto :** Toujours vérifier l'adresse de destination complète sur le dispositif de signature (hardware wallet) avant l'approbation, plutôt que de se contenter de comparer les premiers et derniers caractères de l'adresse copiée.
*   **Surveillance réseau :** Surveiller les requêtes blockchain inhabituelles émises par des applications tierces et suivre les adresses de smart contracts comme indicateurs de compromission (IoC).

---
[Source](https://www.bleepingcomputer.com/news/security/real-emails-hijacked-payments-two-h1-2026-attack-chains/){:target="_blank"}
