---
title: 'New ShadowRay attacks convert Ray clusters into crypto miners'
date: 2025-11-19
permalink: /posts/2025/11/19/new-shadowray-attacks-convert-ray-clusters-into-crypto-miners/
tags:
- veille-cyber
- bleepingcomp
---
## ShadowRay 2.0 : Exploitation de clusters IA pour la minage de cryptomonnaies

Une campagne de cybersécurité nommée ShadowRay 2.0 cible des clusters Ray exposés sur Internet. Les attaquants exploitent une faille de sécurité non corrigée (CVE-2023-48022) pour transformer ces infrastructures de calcul distribué, utilisées pour le développement d'applications IA, en botnets de minage de cryptomonnaies.

Les observations des chercheurs révèlent que cette menace va au-delà du simple minage, incluant potentiellement le vol de données et d'identifiants, ainsi que le lancement d'attaques par déni de service distribué (DDoS). Les charges utiles utilisées dans ces attaques semblent générées par des modèles linguistiques d'IA, d'où l'appellation "ShadowRay 2.0". Elles sont conçues pour se propager de manière autonome entre les clusters compromis.

Les attaquants utilisent la vulnérabilité CVE-2023-48022 pour soumettre des jobs malveillants via l'API Jobs de Ray, déployant des scripts Bash et Python sur tous les nœuds. Le module de minage de cryptomonnaies, utilisant XMRig pour la Monero, est optimisé pour ne consommer que 60% des ressources CPU/GPU afin d'éviter la détection. Des techniques telles que de faux noms de processus (ex: 'dns-filter') et des mécanismes de persistance (cron jobs, modifications de systemd) sont employées pour maintenir leur présence. De plus, les attaquants cherchent à éliminer toute concurrence en bloquant d'autres mineurs et pools de minage.

En dehors du minage, les attaquants établissent des connexions inversées pour un contrôle interactif, permettant l'exfiltration potentielle de données sensibles, d'identifiants MySQL, de modèles IA propriétaires et de code source. Les attaques DDoS sont lancées via l'outil Sockstress.

**Points Clés :**

*   **Cible :** Clusters Ray exposés sur Internet.
*   **Méthode :** Exploitation de la vulnérabilité CVE-2023-48022.
*   **Objectif principal :** Minage de cryptomonnaies.
*   **Fonctionnalités additionnelles :** Vol de données, DDoS.
*   **Technologie :** Utilisation de charges utiles générées par IA.
*   **Propagation :** Autonome entre les clusters.
*   **Persistance :** Mécanismes de longue durée mis en place.

**Vulnérabilités :**

*   **CVE-2023-48022 :** Une faille de sécurité permettant l'exécution de code à distance sur des clusters Ray non protégés.

**Recommandations :**

*   **Isolation :** Déployer Ray exclusivement dans des environnements sécurisés et de confiance, en évitant toute exposition directe sur Internet.
*   **Contrôles d'accès :** Mettre en place des règles de pare-feu et des politiques de groupes de sécurité pour restreindre l'accès non autorisé aux clusters.
*   **Authentification :** Ajouter une couche d'authentification sur le port du tableau de bord Ray (par défaut 8265).
*   **Surveillance :** Implémenter une surveillance continue des clusters d'IA pour détecter les activités anormales.
*   **Mises à jour :** Bien qu'il n'y ait pas de correctif pour CVE-2023-48022, suivre les bonnes pratiques de sécurité recommandées par le fournisseur Anyscale est essentiel.

---
[Source](https://www.bleepingcomputer.com/news/security/new-shadowray-attacks-convert-ray-clusters-into-crypto-miners/){:target="_blank"}
