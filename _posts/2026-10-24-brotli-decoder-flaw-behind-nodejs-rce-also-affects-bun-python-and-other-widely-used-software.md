---
title: 'Brotli Decoder Flaw Behind Node.js RCE Also Affects Bun, Python and Other Widely Used Software'
date: 2026-10-24
permalink: /posts/2026/10/24/brotli-decoder-flaw-behind-nodejs-rce-also-affects-bun-python-and-other-widely-used-software/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans le décodeur Brotli : Menace d'exécution de code à distance

Une corruption de mémoire dans le décodeur de compression Brotli de Google expose de nombreux logiciels à des risques d'exécution de code à distance (RCE), de plantage ou de fuite de mémoire. Bien que l'exploitation nécessite l'envoi de données compressées malveillantes, le risque concerne aussi bien les serveurs traitant des entrées non fiables que les clients effectuant des requêtes HTTP.

**Points clés :**
*   **Vulnérabilité :** Corruption de mémoire permettant potentiellement l'exécution de code arbitraire.
*   **CVE :** CVE-2026-111497.
*   **Gravité :** Évaluée comme critique (9.2 sur l'échelle CVSS 4.0 par Google).
*   **Logiciels impactés :** Node.js, Bun, Envoy, Istio, cdxgen, ainsi que les bibliothèques Python `brotli` et `brotlicffi`.
*   **État actuel :** Aucune exploitation réelle n'a été signalée, mais une preuve de concept (Node2Shell) a démontré la possibilité d'exécuter du code sur des builds de Node.js non patchés.

**Recommandations :**
1.  **Mise à jour immédiate :** Appliquer les correctifs fournis par les éditeurs pour chaque logiciel concerné (voir le tableau des versions corrigées) et redémarrer les services pour charger la version patchée du décodeur.
2.  **Mesures de contingence :**
    *   Si la mise à jour est impossible, désactiver le décodage Brotli pour les entrées non fiables.
    *   Rejeter les requêtes entrantes contenant `Content-Encoding: br`.
    *   En Python, désinstaller les paquets `brotli` et `brotlicffi` pour forcer l'utilisation d'autres formats comme gzip.
3.  **Vérification manuelle :** Ne pas se fier uniquement aux outils de scan de dépendances (comme Dependabot), car certaines entrées d'advisory sont encore en cours de mise à jour pour les paquets spécifiques.

---
[Source](https://thehackernews.com/2026/10/brotli-decoder-flaw-behind-nodejs-rce.html){:target="_blank"}
