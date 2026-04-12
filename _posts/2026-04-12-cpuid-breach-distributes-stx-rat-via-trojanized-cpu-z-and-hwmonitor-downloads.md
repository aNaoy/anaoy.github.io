---
title: 'CPUID Breach Distributes STX RAT via Trojanized CPU-Z and HWMonitor Downloads'
date: 2026-04-12
permalink: /posts/2026/04/12/cpuid-breach-distributes-stx-rat-via-trojanized-cpu-z-and-hwmonitor-downloads/
tags:
- veille-cyber
- hackernews
---
### Compromission du site CPUID : Propagation du cheval de Troie STX RAT

Le site web officiel de CPUID (cpuid.com) a été compromis entre le 9 et le 10 avril, permettant à des cyberattaquants de rediriger les téléchargements de logiciels populaires (CPU-Z, HWMonitor) vers des versions malveillantes. Bien que le site ait été rétabli, plus de 150 victimes ont été identifiées à travers le monde, touchant aussi bien des particuliers que des secteurs industriels et commerciaux.

**Points clés :**
*   **Vecteur d'attaque :** Une vulnérabilité sur une API secondaire a permis de remplacer les liens de téléchargement officiels par des liens redirigeant vers des sites tiers malveillants.
*   **Technique utilisée :** Les attaquants ont eu recours au *DLL side-loading* en incluant un fichier `CRYPTBASE.dll` malveillant aux côtés d'exécutables légitimes signés.
*   **Charge utile :** Le logiciel malveillant déploie **STX RAT**, un cheval de Troie d'accès distant doté de capacités d'espionnage (infostealer), de contrôle à distance (HVNC) et d'exécution de commandes en mémoire.
*   **Attribution :** Les infrastructures de commande et de contrôle (C2) sont identiques à celles utilisées lors de précédentes campagnes visant des logiciels comme FileZilla et 7-Zip, révélant une faible maturité opérationnelle des attaquants.

**Vulnérabilités :**
*   **DLL Side-Loading :** Exploitation du chargement de bibliothèques dynamiques non sécurisé pour exécuter du code arbitraire. Aucune CVE spécifique n'est associée, car il s'agit d'une technique d'exploitation détournant des fonctionnalités légitimes de Windows.

**Recommandations :**
*   **Vérification de l'intégrité :** Pour tout utilisateur ayant téléchargé ces outils entre le 9 et le 10 avril, procéder à une analyse antivirus complète et envisager une réinstallation propre à partir de sources vérifiées.
*   **Surveillance réseau :** Bloquer les connexions sortantes vers les domaines suspects identifiés (notamment `cahayailmukreatif.web[.]id`, `transitopalermo[.]com` et `vatrobran[.]hr`).
*   **Pratiques de téléchargement :** Toujours vérifier la signature numérique des fichiers exécutables téléchargés et privilégier le téléchargement depuis les sites officiels, en surveillant toute anomalie lors de la redirection vers des serveurs tiers (ex: `r2.dev`).

---
[Source](https://thehackernews.com/2026/04/cpuid-breach-distributes-stx-rat-via.html){:target="_blank"}
