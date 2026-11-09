---
title: 'Star Wars Episode I: Racer'
date: 2026-11-09
permalink: /posts/2026/11/09/star-wars-episode-i-racer/
tags:
- veille-cyber
- zerodaysfans
---
# Analyse de sécurité et exécution de code à distance sur Star Wars Episode I: Racer

Cette étude porte sur l'analyse du protocole réseau multijoueur du jeu *Star Wars Episode I: Racer* (version 1.0 GOG), qui utilise l'API Microsoft DirectPlay encapsulée via le projet *ipxwrapper* sur le port UDP 54792.

### Points clés
*   **Analyse protocolaire :** Le jeu communique via des paquets IPX encapsulés dans des datagrammes UDP. L'absence de reconnaissance native par Wireshark a nécessité le développement d'un désassembleur personnalisé pour analyser le trafic.
*   **Mécanisme de communication :** Le jeu utilise des messages système DirectPlay pour la gestion de session et des messages applicatifs personnalisés pour les interactions de jeu.
*   **Vecteur d'attaque :** L'exploitation repose sur l'envoi de paquets réseau contrefaits à un client, tirant parti d'une mauvaise gestion de l'indexation dans les structures de données internes du jeu.

### Vulnérabilité
*   **Description :** Une vulnérabilité de type **Out-of-Bounds Write** (écriture hors limites) a été identifiée dans le traitement des paquets de type 0x21.
*   **CVE :** Aucune CVE n'est mentionnée dans l'article.
*   **Détails techniques :** Le champ `iIndex` dans le paquet réseau permet de sélectionner une structure `STATE_T` dans un tableau fixe. En fournissant un index supérieur ou égal à 20, un attaquant peut écrire des données en dehors de la mémoire allouée au tableau `_g_PlayerStates`.

### Exploitation
L'attaquant peut exploiter cette vulnérabilité en deux étapes :
1.  **Corruption :** Utiliser le message 0x21 pour écraser une entrée dans la table des gestionnaires de réseau (`network_handlers_table`), en détournant le pointeur d'une fonction vers une adresse mémoire contrôlée (le tampon de réception).
2.  **Exécution :** Envoyer un message de type 0x33 contenant un shellcode, qui sera alors exécuté par le jeu suite à la redirection du gestionnaire corrompu.

### Recommandations
*   **Isolement :** Ne pas exposer les services de jeu legacy ou émulés sur des réseaux non fiables ou publics.
*   **Segmentation :** Utiliser des pare-feu pour restreindre l'accès au port 54792 aux seules machines de confiance.
*   **Mise à jour :** Dans le cadre de jeux anciens, appliquer les correctifs communautaires disponibles ou utiliser des conteneurs isolés pour limiter l'impact d'une exécution de code arbitraire sur le système hôte.

---
[Source](https://www.synacktiv.com/en/publications/star-wars-episode-i-racer){:target="_blank"}
