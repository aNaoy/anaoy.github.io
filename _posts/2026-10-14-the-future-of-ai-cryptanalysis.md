---
title: 'The Future of AI Cryptanalysis'
date: 2026-10-14
permalink: /posts/2026/10/14/the-future-of-ai-cryptanalysis/
tags:
- veille-cyber
- schneier
---
### Les risques liés à la cryptanalyse par l'IA et aux vulnérabilités des objets connectés

La sécurité des systèmes cryptographiques est compromise non seulement par la robustesse théorique des algorithmes, mais surtout par la fragilité de leurs implémentations pratiques. L'intégration de code optimisé pour la vitesse introduit fréquemment des canaux auxiliaires (*side channels*) permettant l'exfiltration de données sensibles, une faille exploitée historiquement par des acteurs étatiques et persistant dans les bibliothèques logicielles actuelles.

**Points clés :**
*   **Insécurité des implémentations :** Les compromis de performance dans les bibliothèques cryptographiques (notamment pour AES) créent des fuites de données exploitables à distance.
*   **Pérennité des failles :** Le déploiement massif de dispositifs IoT (compteurs intelligents, dispositifs médicaux) avec des cycles de vie longs rend difficile la correction des vulnérabilités logicielles intégrées.
*   **Émergence des menaces IA :** La miniaturisation des modèles d'IA permet désormais leur exécution sur du matériel IoT limité. Cette capacité ouvre la voie à la création de botnets auto-réplicants autonomes, capables de se propager au-delà des centres de données.

**Vulnérabilités :**
*   **Canaux auxiliaires (*Side-channel attacks*) :** Présents dans de nombreuses implémentations d'AES et de protocoles hérités, ces défauts permettent une fuite de secrets cryptographiques via les routeurs réseau vers le cloud.
*   **Absence de CVE spécifique :** Bien que non listées sous un identifiant unique dans le texte, l'auteur souligne la persistance de vulnérabilités critiques dans les bibliothèques logicielles "Legacy" largement intégrées dans l'IoT.

**Recommandations :**
*   **Auditer l'implémentation :** Ne pas se fier uniquement à la force théorique des algorithmes (y compris pour la cryptographie post-quantique) ; privilégier des implémentations auditées pour leur résistance aux attaques par canaux auxiliaires.
*   **Renforcer la sécurité IoT :** Mettre en place des stratégies de correctifs pour les appareils à longue durée de vie afin de limiter l'exposition aux botnets basés sur l'IA.
*   **Vigilance sur le cycle de vie :** Anticiper le risque que les dispositifs IoT actuels deviennent des vecteurs d'attaques autonomes en raison de leur ubiquité et de leur faible niveau de protection.

---
[Source](https://www.schneier.com/blog/archives/2026/10/the-future-of-ai-cryptanalysis.html){:target="_blank"}
