---
title: 'DeadLock Ransomware Uses Polygon Smart Contracts to Make Extortion Infra Harder to Disrupt'
date: 2026-08-11
permalink: /posts/2026/08/11/deadlock-ransomware-uses-polygon-smart-contracts-to-make-extortion-infra-harder-to-disrupt/
tags:
- veille-cyber
- hackernews
---
### DeadLock : Une infrastructure d'extorsion décentralisée via la blockchain

Le groupe de ransomware DeadLock, actif depuis juillet 2025, se distingue par l'utilisation d'une infrastructure décentralisée basée sur la blockchain Polygon pour mener ses opérations d'extorsion. Contrairement aux groupes traditionnels, DeadLock utilise des contrats intelligents pour rendre son infrastructure de communication et de fuite de données extrêmement résistante aux tentatives de neutralisation.

#### Points clés
*   **Infrastructure résiliente :** Le groupe utilise des fichiers HTML interactifs faisant office d'applications autonomes. Ces fichiers interagissent avec des contrats intelligents sur Polygon pour récupérer dynamiquement les adresses de serveurs proxy, permettant aux attaquants de modifier leurs points de contact sans enregistrer de nouveaux domaines.
*   **Méthodes d'attaque :** Utilisation de la double extorsion (chiffrement et menace de divulgation de données), couplée à un chiffrement hybride (Curve25519 et XChaCha20).
*   **Évasion et furtivité :** Le logiciel malveillant inclut un mécanisme de limitation des ressources pour rester discret, effectue un nettoyage systématique des logs et des clichés instantanés (*Volume Shadow Copies*), et intègre une géolocalisation pour éviter de cibler certains pays (CIS et Moyen-Orient).
*   **Outils de communication :** Les victimes sont dirigées vers l'application de messagerie chiffrée *Session* ou vers le portail HTML intégré pour négocier les paiements en Bitcoin ou Monero.

#### Vulnérabilités exploitées
L'article ne mentionne pas de CVE spécifique, mais souligne l'exploitation des vecteurs suivants :
*   **Manipulation du registre Windows :** Désactivation forcée de la journalisation pour effacer les traces forensiques.
*   **Scripts PowerShell malveillants :** Utilisation de scripts pour supprimer les clichés instantanés (VSS) et arrêter les services critiques.
*   **Abus de services tiers :** Utilisation légitime d'AnyDesk pour la prise de contrôle à distance des hôtes compromis.

#### Recommandations de sécurité
Bien qu'aucune correction logicielle directe ne soit citée pour le ransomware lui-même, les mesures suivantes sont essentielles :
*   **Surveillance des logs :** Implémenter une journalisation centralisée et protégée afin de détecter les tentatives de suppression ou de modification du registre Windows.
*   **Contrôle des services :** Restreindre et surveiller l'exécution de scripts PowerShell, particulièrement ceux tentant d'interagir avec les clichés instantanés ou de stopper les services de sécurité.
*   **Gestion des accès à distance :** Auditer strictement l'utilisation des outils d'administration à distance (comme AnyDesk) au sein du réseau et les bloquer via une liste d'autorisation (*allowlisting*).
*   **Segmentation et sauvegardes :** Maintenir des sauvegardes immuables et déconnectées du réseau principal pour limiter l'impact d'un chiffrement par ransomware.

---
[Source](https://thehackernews.com/2026/08/deadlock-ransomware-uses-polygon-smart.html){:target="_blank"}
