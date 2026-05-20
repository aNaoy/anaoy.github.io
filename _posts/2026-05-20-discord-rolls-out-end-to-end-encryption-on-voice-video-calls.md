---
title: 'Discord rolls out end-to-end encryption on voice, video calls'
date: 2026-05-20
permalink: /posts/2026/05/20/discord-rolls-out-end-to-end-encryption-on-voice-video-calls/
tags:
- veille-cyber
- bleepingcomp
---
# Généralisation du chiffrement de bout en bout sur Discord

Discord a officialisé le déploiement généralisé du chiffrement de bout en bout (E2EE) pour l'ensemble de ses appels vocaux et vidéo, y compris les messages privés, les groupes et les diffusions « Go Live ».

### Points clés
*   **Protocole utilisé :** Le protocole open-source **DAVE** (basé sur le standard MLS pour les échanges de clés de groupe et WebRTC).
*   **Couverture :** La mesure s'applique par défaut, sans option à activer, sur toutes les plateformes (Desktop, Mobile, Web, consoles Xbox/PlayStation).
*   **Exception :** Les « Stage Channels » (salons de scène) restent exclus du chiffrement, étant conçus pour des diffusions publiques à grande échelle.
*   **Messages texte :** Le chiffrement de bout en bout n'est pas prévu pour les discussions textuelles en raison de contraintes architecturales majeures liées à la conception initiale de la plateforme.

### Vulnérabilités
*   Aucune CVE spécifique n'est mentionnée. L'article se concentre sur l'amélioration proactive de la confidentialité. Une collaboration technique avec Mozilla a été nécessaire pour résoudre une incompatibilité de compatibilité avec le navigateur Firefox lors de l'implémentation.

### Recommandations
*   **Utilisateurs :** Aucune action requise, le chiffrement est activé nativement par mise à jour automatique.
*   **Sécurité générale :** Bien que les appels soient désormais sécurisés par le protocole DAVE, il est rappelé que les communications textuelles ne bénéficient pas de cette protection. Les utilisateurs manipulant des données hautement sensibles doivent privilégier des canaux de communication nativement chiffrés pour le texte (comme Signal) plutôt que les fonctionnalités textuelles de Discord.

---
[Source](https://www.bleepingcomputer.com/news/security/discord-rolls-out-end-to-end-encryption-on-voice-video-calls/){:target="_blank"}
