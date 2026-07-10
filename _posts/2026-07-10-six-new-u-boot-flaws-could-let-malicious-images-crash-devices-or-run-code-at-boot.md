---
title: 'Six New U-Boot Flaws Could Let Malicious Images Crash Devices or Run Code at Boot'
date: 2026-07-10
permalink: /posts/2026/07/10/six-new-u-boot-flaws-could-let-malicious-images-crash-devices-or-run-code-at-boot/
tags:
- veille-cyber
- hackernews
---
### Six failles critiques découvertes dans le chargeur de démarrage U-Boot

Des chercheurs de la société Binarly ont identifié six vulnérabilités majeures dans U-Boot, le chargeur de démarrage utilisé par une vaste gamme d'appareils (routeurs, caméras connectées, serveurs). Ces failles sont exploitables lors du traitement des images de démarrage (FIT - Flattened Image Tree) avant la vérification de leur signature numérique, permettant ainsi de compromettre la chaîne de confiance au niveau le plus bas du matériel.

**Points clés :**
* **Nature des vulnérabilités :** Deux failles permettent l'exécution de code arbitraire, tandis que quatre autres provoquent le plantage (déni de service) de l'appareil.
* **Impact :** L'exécution de code au stade du bootloader compromet la sécurité de l'ensemble du système d'exploitation, car elle survient avant toute mesure de protection logicielle.
* **Historique :** Le code vulnérable est présent depuis la version 2013.07, rendant une multitude de firmwares tiers potentiellement exposés.
* **Disponibilité :** Les correctifs ont été intégrés dans le code source d'U-Boot en juin, mais ne seront pas inclus dans une version stable avant octobre 2026.

**Vulnérabilités identifiées (IDs Binarly) :**
* **Exécution de code :** BRLY-2026-037, BRLY-2026-038 (liées à un défaut de vérification sur `fdt_get_name`).
* **Déni de service (crash) :** BRLY-2026-039, BRLY-2026-040, BRLY-2026-041, BRLY-2026-042.
* *Note : Aucun identifiant CVE n'a encore été attribué à ces vulnérabilités.*

**Recommandations :**
* **Pour les constructeurs et mainteneurs :** Ne pas attendre la prochaine version officielle d'U-Boot. Il est impératif d'intégrer immédiatement les correctifs disponibles via les liens de commit fournis dans les avis de Binarly.
* **Pour les utilisateurs finaux :** Surveiller les mises à jour de firmware publiées par les fournisseurs des appareils concernés. La remédiation dépendra exclusivement de la rapidité avec laquelle ces derniers diffuseront les correctifs sur leurs produits.

---
[Source](https://thehackernews.com/2026/07/six-new-u-boot-flaws-could-let.html){:target="_blank"}
