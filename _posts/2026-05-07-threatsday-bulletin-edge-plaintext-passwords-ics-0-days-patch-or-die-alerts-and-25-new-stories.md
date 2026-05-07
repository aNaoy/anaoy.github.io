---
title: 'ThreatsDay Bulletin: Edge Plaintext Passwords, ICS 0-Days, Patch-or-Die Alerts and 25+ New Stories'
date: 2026-05-07
permalink: /posts/2026/05/07/threatsday-bulletin-edge-plaintext-passwords-ics-0-days-patch-or-die-alerts-and-25-new-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces et vulnérabilités (Mai 2026)

Le paysage cyber actuel est marqué par une industrialisation des attaques, où l'IA accélère la détection de vulnérabilités et l'automatisation des compromissions.

#### Points clés
*   **Accélération des vulnérabilités :** Le délai entre la découverte d'une faille et son exploitation a chuté drastiquement (44 jours en moyenne). Des modèles d'IA (type *Anthropic Mythos*) sont désormais utilisés pour identifier des failles à grande échelle.
*   **Chaînes d'approvisionnement :** Multiplication des campagnes de *typosquatting* (NuGet, GitHub) et utilisation de malwares développés en Rust.
*   **Campagnes de fraude :** Recrudescence de malwares financiers sur Android (+67 %) et campagnes de phishing par SMS (*smishing*) mondiales.
*   **Réponse institutionnelle :** Le gouvernement américain envisage de réduire les délais de correction des failles critiques à 72 heures.

#### Vulnérabilités critiques
*   **Eclipse BaSyx V2 :** 
    *   **CVE-2026-7411 (CVSS 10.0) :** Traversée de chemin permettant l'exécution de code arbitraire.
    *   **CVE-2026-7412 (CVSS 8.6) :** SSRF permettant de pivoter vers des systèmes industriels isolés (PLCs).
*   **MOVEit Automation :** 
    *   **CVE-2026-4670 (CVSS 9.8) :** Contournement d'authentification critique permettant un contrôle administratif.
*   **Salesforce Marketing Cloud :** Série de failles (dont **CVE-2026-22585/86/82/83**) permettant la fuite de bases de données de contacts et l'accès aux communications.
*   **Microsoft Edge :** Exposition de mots de passe en clair dans la mémoire vive, accessibles aux utilisateurs disposant de privilèges administratifs.

#### Recommandations
*   **Hygiène logicielle :** Adopter des outils comme `pnpm 11` qui imposent un délai de rétention de 24h avant l'installation de nouveaux paquets pour limiter les risques liés à la chaîne d'approvisionnement.
*   **Gestion des correctifs :** Réviser les cycles de maintenance pour intégrer des déploiements de sécurité mensuels (notamment pour les produits Oracle) et viser une réactivité accrue face aux failles critiques.
*   **Sécurisation des accès :** Désactiver les fonctionnalités d'IA sur appareil dans les navigateurs si elles ne sont pas nécessaires pour limiter les vecteurs de télémétrie et d'installation silencieuse.
*   **Vigilance utilisateur :** Se méfier systématiquement des résultats sponsorisés sur les moteurs de recherche (phishing par *Ad-inject*) et vérifier l'origine des installations logicielles (GitHub, sites officiels).

---
[Source](https://thehackernews.com/2026/05/threatsday-bulletin-edge-plaintext.html){:target="_blank"}
