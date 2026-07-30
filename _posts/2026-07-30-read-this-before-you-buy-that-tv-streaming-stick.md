---
title: 'Read This Before You Buy That TV Streaming Stick'
date: 2026-07-30
permalink: /posts/2026/07/30/read-this-before-you-buy-that-tv-streaming-stick/
tags:
- veille-cyber
- krebs
---
### La menace des boîtiers TV bon marché : botnets et fraude publicitaire

Une analyse menée par la société de cybersécurité Bitsight révèle que de nombreux boîtiers de streaming TV « génériques » (notamment la marque **H96**) sont livrés avec des portes dérobées préinstallées. Ces appareils sont exploités à l'insu des utilisateurs pour mener des activités frauduleuses à grande échelle.

**Points clés :**
*   **Fraude publicitaire automatisée :** Les appareils simulent le comportement de smartphones (spoofing) pour cliquer sur des publicités hébergées sur des sites générés par intelligence artificielle.
*   **Double fonction malveillante :** Lorsque le boîtier est utilisé (signal HDMI détecté), il sert de nœud de sortie pour des réseaux de procuration résidentielle (proxy). Lorsqu'il est en veille, il bascule en mode botnet pour la fraude publicitaire.
*   **Opérateur identifié :** Les activités sont liées à la société chinoise *Zhejiang Fengwo IoT Technology Ltd* (Fengwo Group), qui utilise des outils de programmation visuelle (Blockly) pour automatiser la création de sites frauduleux et réduire les coûts opérationnels.
*   **Envergure :** Le réseau toucherait des dizaines de milliers d'appareils, générant des revenus estimés à plus de 50 000 $ par jour.

**Vulnérabilités :**
L'article pointe une insécurité structurelle des boîtiers bas de gamme :
*   **Absence d'authentification :** Ces appareils ne disposent pas de protocoles de sécurité robustes, permettant une prise de contrôle facile par des botnets (ex: botnet *Kimwolf*).
*   **Logiciels préinstallés malveillants :** Intégration native de logiciels de proxy résidentiel et de backdoors de télémétrie.
*   *Note : Aucune CVE spécifique n'est mentionnée, car il s'agit de comportements conçus dès la fabrication du firmware ("factory backdoor").*

**Recommandations :**
*   **Privilégier des marques reconnues :** Éviter les boîtiers de streaming "génériques" ou sans marque vendus à prix cassé.
*   **Vérifier la certification :** S'assurer que l'appareil possède la certification officielle **Android TV OS** et **Play Protect** (via le support Google).
*   **Consulter les listes d'alerte :** Se référer aux travaux de recherche publique (comme ceux de *Synthient*) qui répertorient les modèles d'objets connectés (IoT) connus pour contenir des logiciels de proxy indésirables.
*   **Prudence avec les applications tierces :** Même sur des appareils de marque, limiter l'installation d'applications non vérifiées qui pourraient dissimuler des services de proxy.

---
[Source](https://krebsonsecurity.com/2026/07/read-this-before-you-buy-that-tv-streaming-stick/){:target="_blank"}
