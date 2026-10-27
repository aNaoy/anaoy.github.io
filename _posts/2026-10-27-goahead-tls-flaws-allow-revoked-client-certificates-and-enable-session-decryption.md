---
title: 'GoAhead TLS Flaws Allow Revoked Client Certificates and Enable Session Decryption'
date: 2026-10-27
permalink: /posts/2026/10/27/goahead-tls-flaws-allow-revoked-client-certificates-and-enable-session-decryption/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques du serveur web GoAhead

Le serveur web embarqué GoAhead, utilisé dans des millions d'appareils (routeurs, imprimantes, contrôleurs industriels), présente plusieurs failles de sécurité critiques au niveau de son implémentation TLS et de son mécanisme d'authentification.

#### Points clés
*   **Nature des risques :** Les failles permettent le contournement de l'authentification par certificat, le déchiffrement de sessions TLS et des accès non autorisés.
*   **Répartition par backend :** Les vulnérabilités dépendent du moteur TLS choisi lors de la compilation du firmware par le fabricant.
*   **Mise à jour :** La version 6.1.1 corrige ces problèmes. Toutefois, la correction nécessite une mise à jour du firmware par le fabricant de l'appareil, rendant les utilisateurs finaux dépendants de leur réactivité.

#### Vulnérabilités identifiées

| Composant | Problème | CVE | Sévérité |
| :--- | :--- | :--- | :--- |
| **OpenSSL** | La liste de révocation (CRL) est chargée mais jamais appliquée, permettant l'usage de certificats révoqués. | CVE-2026-115881 | 9.1 |
| **LibreSSL** | Acceptation de chaînes de certificats trop longues, contournant les limites de sécurité. | CVE-2026-115884 | 7.4 |
| **Mbed TLS** | Erreur de longueur de clé DHE permettant à un attaquant passif de déchiffrer la session. | N/A | 5.9 |
| **Authentification** | Contournement du login : possibilité de se connecter avec n'importe quel mot de passe si celui-ci utilise le format Blowfish. | N/A | Critique |

#### Recommandations
*   **Pour les fabricants :** Mettre à jour GoAhead vers la version **6.1.1** et diffuser les correctifs via des mises à jour de firmware.
*   **Pour les administrateurs/utilisateurs :** 
    *   Vérifier les mises à jour disponibles auprès des fabricants de vos équipements.
    *   Après mise à jour vers la v6.1.1 : réinitialiser les sessions actives, redémarrer le serveur et procéder à un changement des mots de passe utilisant le format Blowfish.
    *   En attendant un correctif, lorsque cela est possible : privilégier l'utilisation du backend OpenSSL (sauf si vulnérable) ou désactiver les suites de chiffrement DHE à champs finis sur les builds Mbed TLS.

---
[Source](https://thehackernews.com/2026/10/goahead-tls-flaws-allow-revoked-client.html){:target="_blank"}
