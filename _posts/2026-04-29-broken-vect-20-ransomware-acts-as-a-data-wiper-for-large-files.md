---
title: 'Broken VECT 2.0 ransomware acts as a data wiper for large files'
date: 2026-04-29
permalink: /posts/2026/04/29/broken-vect-20-ransomware-acts-as-a-data-wiper-for-large-files/
tags:
- veille-cyber
- bleepingcomp
---
### VECT 2.0 : Un ransomware défectueux agissant comme un destructeur de données

Le ransomware VECT 2.0, distribué via BreachForums et lié au groupe malveillant TeamPCP, présente une faille de conception critique dans son processus de chiffrement. Plutôt que de chiffrer les fichiers de manière réversible, le malware provoque la destruction permanente des données pour tout fichier dépassant 128 Ko.

**Points clés :**
*   **Erreur technique :** Lors du traitement des fichiers volumineux, le malware réutilise le même tampon mémoire pour stocker les "nonces" de chiffrement. Chaque nouveau bloc écrase le précédent.
*   **Résultat irréversible :** Seuls les 25 % finaux du fichier peuvent être déchiffrés. Les 75 % restants sont irrécupérables, car les nonces nécessaires au déchiffrement ne sont jamais conservés ni transmis aux attaquants.
*   **Impact opérationnel :** La quasi-totalité des fichiers critiques d'une entreprise (bases de données, machines virtuelles, sauvegardes et documents courants) dépasse le seuil de 128 Ko, rendant le ransomware, par accident, destructeur (wiper).
*   **Portée :** La faille est présente dans toutes les variantes du logiciel, qu'elles ciblent Windows, Linux ou ESXi.

**Vulnérabilités :**
*   Aucun identifiant CVE n'est associé à cette faille, car il s'agit d'une erreur de programmation logique dans le code source du malware lui-même et non d'une vulnérabilité logicielle exploitée.

**Recommandations :**
*   **Stratégie de sauvegarde :** Maintenir des sauvegardes immuables et déconnectées du réseau (air-gapped), car même en payant la rançon, les opérateurs de VECT 2.0 sont techniquement incapables de restaurer les fichiers endommagés.
*   **Sécurité de la chaîne d'approvisionnement :** Vigilance accrue face aux logiciels tiers, le groupe TeamPCP étant spécialisé dans l'empoisonnement de dépôts (type PyPI/GitHub) pour introduire des payloads malveillants.
*   **Détection :** Mettre en œuvre des solutions de détection d'anomalies sur le stockage pour identifier rapidement les processus de chiffrement/destruction massive de fichiers et isoler les systèmes infectés avant que le processus ne s'achève.

---
[Source](https://www.bleepingcomputer.com/news/security/broken-vect-20-ransomware-acts-as-a-data-wiper-for-large-files/){:target="_blank"}
