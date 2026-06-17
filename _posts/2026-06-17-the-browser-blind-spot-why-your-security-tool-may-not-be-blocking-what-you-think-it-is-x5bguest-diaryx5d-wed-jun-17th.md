---
title: 'The browser blind spot: Why your security tool may not be blocking what you think it is &#x5b;Guest Diary&#x5d;, (Wed, Jun 17th)'
date: 2026-06-17
permalink: /posts/2026/06/17/the-browser-blind-spot-why-your-security-tool-may-not-be-blocking-what-you-think-it-is-x5bguest-diaryx5d-wed-jun-17th/
tags:
- veille-cyber
- sans-isc
---
### L’angle mort des CASB : Le protocole QUIC et le contournement des politiques de sécurité

Les solutions CASB (*Cloud Access Security Broker*) reposent traditionnellement sur l'inspection du trafic TCP. Cependant, l'adoption généralisée du protocole **QUIC (HTTP/3)**, qui s'exécute sur le protocole **UDP**, crée une faille majeure : le trafic utilisant QUIC contourne les proxies, rendant les politiques de blocage inopérantes et invisibles dans les journaux d'audit.

**Points clés :**
*   **Invisibilité totale :** Lorsqu'un navigateur (Chrome, Edge, Brave) utilise QUIC pour atteindre un site, le CASB ne "voit" aucune connexion. Aucun blocage n'est déclenché et aucune trace n'apparaît dans les logs, donnant une fausse impression de sécurité.
*   **Hétérogénéité des navigateurs :** Les politiques de sécurité sont souvent validées sur un seul navigateur. Or, chaque moteur de rendu gère le protocole QUIC différemment, permettant à certains navigateurs de contourner les contrôles là où d'autres échouent.
*   **Risque de conformité :** Ce contournement facilite l'utilisation non autorisée d'outils (IA générative, stockage cloud) sur des postes gérés, exposant les entreprises à des fuites de données et des risques réglementaires (RGPD, HIPAA, SOC 2).

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle avec CVE spécifique, mais d'une **faille de conception structurelle** entre les protocoles de transport (UDP/QUIC) et les outils d'inspection basés sur TCP (Proxy/CASB).

**Recommandations :**
1.  **Bloquer le protocole QUIC au niveau réseau :** Configurer les pare-feu ou passerelles web (SWG) pour rejeter tout trafic sortant sur le port **UDP/443**. Cela forcera les navigateurs à basculer vers le protocole TCP, permettant ainsi au CASB d'intercepter et d'inspecter le trafic.
2.  **Tester systématiquement tous les navigateurs :** Ne pas se limiter à un seul navigateur lors de la validation des règles. Tester individuellement Safari, Chrome, Edge, Brave et Firefox.
3.  **Corréler les logs :** Ne pas se fier uniquement aux journaux du CASB. Comparer ces logs avec les données télémétriques des endpoints pour identifier les disparités entre le trafic attendu et le trafic réellement inspecté.
4.  **Adopter des solutions natives au navigateur :** En complément du CASB, envisager des outils de sécurité "browser-native" (DLP intégré au navigateur ou navigateurs sécurisés d'entreprise) pour appliquer des politiques de contrôle indépendamment du protocole de transport réseau.

---
[Source](https://isc.sans.edu/diary/rss/33084){:target="_blank"}
