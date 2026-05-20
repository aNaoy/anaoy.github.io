---
title: 'Grafana breach caused by missed token rotation after TanStack attack'
date: 2026-05-20
permalink: /posts/2026/05/20/grafana-breach-caused-by-missed-token-rotation-after-tanstack-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Failles dans la rotation des jetons : le piratage de Grafana via la chaîne d'approvisionnement

L'incident de sécurité chez Grafana Labs découle de la campagne de logiciels malveillants « Shai-Hulud », où des attaquants (le groupe TeamPCP) ont compromis des paquets npm légitimes (TanStack). En intégrant ces paquets infectés dans leur environnement CI/CD, Grafana a vu ses jetons GitHub exfiltrés vers les attaquants. Malgré une réponse immédiate, l'oubli d'un jeton spécifique lors de la procédure de rotation a permis aux cybercriminels d'accéder à des dépôts privés, entraînant le vol de code source et d'informations opérationnelles, bien que les données de production des clients demeurent intactes.

**Points clés**
* **Origine :** Attaque par empoisonnement de la chaîne d'approvisionnement logicielle via des paquets npm corrompus.
* **Impact technique :** Exfiltration de jetons GitHub workflow, permettant un accès non autorisé à des dépôts privés et à des données professionnelles (noms/emails).
* **Conséquences :** Aucun impact sur les systèmes de production ou les données des clients de Grafana Cloud. Le code source est resté intègre et n'a pas été altéré.

**Vulnérabilités**
* **Supply-Chain Attack :** Utilisation de dépendances tierces malveillantes (packages npm TanStack) pour l'exécution de code à distance (info-stealer) dans l'environnement CI/CD.
* **Gestion des secrets :** Échec du processus de remédiation (rotation des jetons) dû à l'oubli d'un jeton de workflow GitHub critique.

**Recommandations**
* **Audit des dépendances :** Renforcer la surveillance et la vérification de l'intégrité des paquets tiers utilisés dans les pipelines de déploiement.
* **Automatisation de la révocation :** Mettre en place des processus de révocation de secrets plus robustes et automatisés lors de la détection d'une compromission, pour éviter les omissions humaines.
* **Principe du moindre privilège :** Restreindre les permissions des jetons GitHub workflow au strict nécessaire pour limiter les dommages en cas de fuite.

---
[Source](https://www.bleepingcomputer.com/news/security/grafana-breach-caused-by-missed-token-rotation-after-tanstack-attack/){:target="_blank"}
