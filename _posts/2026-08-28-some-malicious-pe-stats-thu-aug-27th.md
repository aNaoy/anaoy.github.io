---
title: 'Some Malicious PE Stats, (Thu, Aug 27th)'
date: 2026-08-28
permalink: /posts/2026/08/28/some-malicious-pe-stats-thu-aug-27th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des métadonnées des exécutables malveillants

Une étude menée sur plus de 690 000 fichiers PE (Portable Executable) malveillants issus de Malware Bazaar permet d'établir une cartographie des outils de compilation privilégiés par les attaquants. En utilisant des techniques d'analyse de "Rich Header", de structures CLR et de signatures heuristiques, cette recherche offre des données précieuses pour le clustering de campagnes malveillantes.

**Points clés :**
*   **Prédominance du 32 bits :** Malgré l'évolution technologique, les fichiers malveillants 32 bits restent nettement plus fréquents que les 64 bits.
*   **Prévalence du toolchain Microsoft :** Une part importante des malwares est compilée avec Visual C/C++, identifiable via les « Rich Headers ».
*   **Adoption des langages modernes :** Contrairement aux attentes, des langages comme Go (0,9 %) et Rust (0,2 %) restent marginaux dans les échantillons analysés.
*   **Diversité des compilateurs :** L'analyse identifie également l'usage régulier de Borland C++/Delphi (2,9 %) et de GCC/MinGW (2,0 %).

**Vulnérabilités et limites techniques :**
*   **Falsification de métadonnées :** Les en-têtes PE ne sont pas fiables ; les attaquants peuvent manipuler ou supprimer les « Rich Headers » pour entraver l'analyse forensique ou tromper les outils de détection.
*   **Absence de CVE directe :** Cette étude porte sur l'analyse statique des binaires et ne révèle pas de vulnérabilité logicielle spécifique (CVE) liée aux compilateurs eux-mêmes.

**Recommandations :**
*   **Méfiance systématique :** Ne jamais se fier aveuglément aux métadonnées (en-têtes, timestamps) d'un exécutable suspect, car celles-ci sont facilement altérables.
*   **Utilisation d'outils spécialisés :** Pour l'analyse forensique, utiliser des outils capables de parser les structures PE complexes (comme *pefile* ou *Detect It Easy*) afin d'identifier des incohérences ou des patterns de compilation.
*   **Clustering basé sur le build :** Pour les analystes SOC/CERT, exploiter les identifiants de build des « Rich Headers » pour regrouper des échantillons provenant potentiellement des mêmes environnements de développement ou campagnes d'attaques.

---
[Source](https://isc.sans.edu/diary/rss/33292){:target="_blank"}
