---
title: 'New ShadowRay attacks convert Ray clusters into crypto miners'
date: 2025-11-19
permalink: /posts/2025/11/19/new-shadowray-attacks-convert-ray-clusters-into-crypto-miners/
tags:
- veille-cyber
- bleepingcomp
---
## Menace ShadowRay 2.0 : Des grappes Ray détournées pour le minage de cryptomonnaies

Une campagne malveillante baptisée ShadowRay 2.0 exploite une faille ancienne et non corrigée dans les clusters Ray, des plateformes de calcul distribué pour applications IA et Python. L'attaquant, identifié comme IronErn440, utilise des charges utiles générées par intelligence artificielle pour transformer ces infrastructures accessibles publiquement en botnets de minage de cryptomonnaies.

Les activités vont au-delà du simple minage, incluant également le vol de données et d'identifiants, ainsi que le lancement d'attaques par déni de service distribué (DDoS). La campagne actuelle s'appuie sur deux vagues, l'une utilisant GitLab pour la distribution des charges utiles, l'autre, en cours, utilisant GitHub.

### Points Clés :

*   **Exploitation d'une vulnérabilité critique non corrigée** : CVE-2023-48022.
*   **Utilisation de charges utiles générées par IA** : Le code malveillant montre des signes de génération par des modèles linguistiques de grande taille.
*   **Propagation autonome** : Le malware se déploie sur tous les nœuds du cluster et peut se propager de cluster à cluster.
*   **Minage de cryptomonnaies (Monero)** : Utilisation du mineur XMRig, optimisé pour rester discret en limitant l'utilisation des ressources et en usurpant des noms de processus.
*   **Vol de données et contrôle à distance** : Mise en place de shells inversés pour l'exfiltration de données sensibles, d'identifiants et de modèles IA.
*   **Attaques DDoS** : Utilisation de l'outil Sockstress.
*   **Persistance** : Mécanismes mis en place via des tâches cron et des modifications du système.
*   **Exclusivité des ressources** : L'attaquant élimine les autres mineurs et bloque les pools concurrents.

### Vulnérabilités :

*   **CVE-2023-48022** : Vulnérabilité d'exécution de code permettant l'exploitation de l'API Jobs non authentifiée de Ray.

### Recommandations :

*   **Déploiement dans un environnement sécurisé** : Utiliser Ray uniquement dans des réseaux de confiance et strictement contrôlés.
*   **Protection des clusters** : Mettre en place des règles de pare-feu et des politiques de groupe de sécurité pour empêcher tout accès non autorisé.
*   **Authentification du Dashboard Ray** : Ajouter une couche d'autorisation sur le port par défaut du tableau de bord Ray (8265).
*   **Surveillance continue** : Mettre en œuvre une surveillance active des clusters IA pour détecter toute activité anormale.
*   **Application des bonnes pratiques** : Suivre les recommandations du fournisseur Anyscale pour le déploiement sécurisé de Ray.

---
[Source](https://www.bleepingcomputer.com/news/security/new-shadowray-attacks-convert-ray-clusters-into-crypto-miners/){:target="_blank"}
