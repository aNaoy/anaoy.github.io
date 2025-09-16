---
title: 'Phoenix RowHammer Attack Bypasses Advanced DDR5 Memory Protections in 109 Seconds'
date: 2025-09-16
permalink: /posts/2025/09/16/phoenix-rowhammer-attack-bypasses-advanced-ddr5-memory-protections-in-109-seconds/
tags:
- veille-cyber
- hackernews
---
## Phoenix : Une Nouvelle Attaque RowHammer Contourne les Protections DDR5

Une variante de l'attaque RowHammer, baptisée Phoenix (CVE-2025-6202), a été découverte par des chercheurs d'ETH Zürich et de Google. Cette attaque exploite une vulnérabilité matérielle qui permet de corrompre des données en effectuant des accès répétés à des lignes de mémoire DRAM. Phoenix se distingue par sa capacité à contourner les mécanismes de défense avancés mis en place dans les puces mémoire DDR5 de SK Hynix, y compris les protections On-die ECC (Error Correction Code) et TRR (Target Row Refresh).

Dans un cas de test, l'attaque a réussi à provoquer des modifications de bits sur tous les modules DDR5 échantillonnés en 109 secondes seulement, aboutissant à une élévation de privilèges vers l'utilisateur root sur un système standard équipé de DDR5. Les scénarios d'exploitation potentiels incluent le vol de clés RSA-2048 de machines virtuelles pour compromettre l'authentification SSH, ou l'utilisation du binaire sudo pour obtenir des droits d'administrateur local.

Cette découverte souligne que les vulnérabilités RowHammer persistent malgré les améliorations des technologies mémoire, et que les dispositifs existants resteront vulnérables pendant de nombreuses années car ils ne sont pas mis à jour.

**Points Clés :**

*   **Nouvelle variante d'attaque RowHammer :** Phoenix (CVE-2025-6202).
*   **Ciblage :** Puces mémoire DDR5 de SK Hynix.
*   **Capacité :** Contourne les protections avancées comme On-die ECC et TRR.
*   **Impact :** Corruption de données, élévation de privilèges (root) en 109 secondes.
*   **Scénarios d'exploitation :** Vol de clés cryptographiques, accès root local.
*   **Persistance de la vulnérabilité :** Les puces mémoires existantes ne peuvent être mises à jour.

**Vulnérabilités :**

*   **Phoenix :** CVE-2025-6202 (CVSS score : 7.1)
    *   Permet de contourner les protections On-die ECC et TRR sur les mémoires DDR5.
    *   Provoque des modifications de bits ("bit flips") dans les lignes de mémoire adjacentes aux lignes fréquemment sollicitées.

**Recommandations :**

*   Augmenter le taux de rafraîchissement de la mémoire DRAM à 3x.

---
[Source](https://thehackernews.com/2025/09/phoenix-rowhammer-attack-bypasses.html){:target="_blank"}
