---
title: 'Why Secure Data Movement Is the Zero Trust Bottleneck Nobody Talks About'
date: 2026-04-28
permalink: /posts/2026/04/28/why-secure-data-movement-is-the-zero-trust-bottleneck-nobody-talks-about/
tags:
- veille-cyber
- hackernews
---
### Le goulot d'étranglement méconnu du Zero Trust : la sécurisation du transfert de données

Le modèle Zero Trust se concentre souvent excessivement sur l'identité et les points de terminaison, négligeant le défi critique du transfert sécurisé des données entre environnements (IT/OT, cloud, réseaux classifiés). Cette faille, aggravée par le maintien de processus manuels dans plus de 50 % des organisations de sécurité nationale, crée un écart de performance que les attaquants exploitent activement.

**Points clés :**
*   **Obsolescence des processus :** 78 % des organisations considèrent les infrastructures héritées et les processus manuels comme leurs principales vulnérabilités.
*   **Disparition du « Air Gap » :** La convergence entre les réseaux IT et OT (70 % des systèmes OT connectés à l'IT) élargit considérablement la surface d'attaque.
*   **Le mythe du compromis vitesse/sécurité :** L'incapacité à automatiser la sécurisation des flux de données freine l'adoption de l'IA et des prises de décision en temps réel.
*   **Risque lié aux tiers :** Les vulnérabilités des solutions de transfert de fichiers gérés (MFT) sont devenues des vecteurs d'attaque majeurs.

**Vulnérabilités mentionnées :**
*   **Failles dans les outils de transfert de fichiers (MFT) :** L'article cite l'exploitation massive des vulnérabilités dans **MOVEit**, **GoAnywhere** et **Cleo** (ex: CVE-2023-34362 pour MOVEit), illustrant comment les attaquants ciblent les "tuyaux" de transfert de données.

**Recommandations :**
*   **Adoption d'une architecture multicouche :** Combiner trois piliers fondamentaux : le **Zero Trust** (gouvernance des accès), la **sécurité centrée sur la donnée** (protection intrinsèque du contenu) et les **solutions Cross-Domain** (sécurisation dynamique des transferts entre domaines de confiance différents).
*   **Automatisation des contrôles :** Déplacer les mécanismes de validation, de filtrage et de contrôle de politique directement aux frontières des réseaux pour permettre un flux sécurisé à la vitesse du besoin opérationnel.
*   **Intégrité en transit :** Prioriser des solutions capables de garantir l'intégrité des données et d'empêcher toute altération lors du passage entre des environnements aux niveaux de classification ou de sécurité divergents.

---
[Source](https://thehackernews.com/2026/04/why-secure-data-movement-is-zero-trust.html){:target="_blank"}
