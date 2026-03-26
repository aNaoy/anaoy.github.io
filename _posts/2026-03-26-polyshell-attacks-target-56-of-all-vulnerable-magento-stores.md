---
title: 'PolyShell attacks target 56% of all vulnerable Magento stores'
date: 2026-03-26
permalink: /posts/2026/03/26/polyshell-attacks-target-56-of-all-vulnerable-magento-stores/
tags:
- veille-cyber
- bleepingcomp
---
### Vague d'attaques PolyShell sur Magento : exécution de code et vol de données

La faille critique « PolyShell » affectant Magento Open Source et Adobe Commerce fait l'objet d'une exploitation massive. Depuis sa divulgation publique le 17 mars 2026, plus de 56 % des boutiques vulnérables ont déjà été ciblées. Les attaquants utilisent cette vulnérabilité pour injecter des logiciels malveillants, notamment un nouveau type de « skimmer » (collecteur de données bancaires) sophistiqué.

**Points clés :**
*   **Vulnérabilité API :** L'API REST de Magento permet le téléversement de fichiers « polyglottes » via les options personnalisées des articles de panier.
*   **Exfiltration furtive :** Les attaquants déploient un *skimmer* utilisant le protocole **WebRTC**. En privilégiant le trafic UDP chiffré par rapport au trafic HTTP standard, cette méthode contourne les politiques de sécurité de contenu (CSP) classiques.
*   **Techniques d'évasion :** Le *skimmer* retarde son exécution pour éviter la détection et utilise des échanges SDP contrefaits pour communiquer avec ses serveurs de commande et de contrôle (C2).

**Vulnérabilités :**
*   **PolyShell :** Faille d'exécution de code à distance (RCE) non authentifiée via l'API REST de Magento. (CVE non encore assignée formellement dans l'article, bien que la faille soit identifiée).

**Recommandations :**
*   **Surveillance :** Inspecter les journaux serveur à la recherche des adresses IP malveillantes recensées par Sansec.
*   **Mise à jour :** Bien qu'Adobe ait intégré un correctif dans la version 2.4.9-beta1, aucune version stable pour la production n'est disponible à ce jour. En attendant, renforcer les configurations de serveur pour limiter les accès API et restreindre les capacités de téléversement.
*   **Analyse des indicateurs :** Utiliser les indicateurs de compromission (IoC) fournis par Sansec pour vérifier si des scripts non autorisés (particulièrement ceux utilisant WebRTC) sont présents sur la plateforme.

---
[Source](https://www.bleepingcomputer.com/news/security/polyshell-attacks-target-56-percent-of-all-vulnerable-magento-stores/){:target="_blank"}
