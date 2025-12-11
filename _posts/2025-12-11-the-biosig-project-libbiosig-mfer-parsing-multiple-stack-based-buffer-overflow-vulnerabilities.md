---
title: 'The Biosig Project libbiosig MFER parsing multiple stack-based buffer overflow vulnerabilities'
date: 2025-12-11
permalink: /posts/2025/12/11/the-biosig-project-libbiosig-mfer-parsing-multiple-stack-based-buffer-overflow-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
**Vulnérabilités critiques dans libbiosig : Risque d'exécution de code arbitraire via des fichiers MFER malveillants**

Des vulnérabilités de débordement de tampon basé sur la pile ont été découvertes dans la fonction de parsing MFER de la bibliothèque libbiosig (version 3.9.1) du projet Biosig. Ces failles permettent à un attaquant de provoquer une exécution de code arbitraire en fournissant un fichier MFER spécialement conçu.

**Points clés :**

*   **Bibliothèque affectée :** The Biosig Project libbiosig version 3.9.1.
*   **Type de fichier vulnérable :** Fichiers au format MFER (Medical waveform Format Encoding Rules).
*   **Mécanisme d'attaque :** Le traitement incorrect des longueurs de données dans les fichiers MFER peut entraîner des dépassements de tampon basés sur la pile lors de la lecture de données.
*   **Impact :** Exécution de code arbitraire à distance avec un score CVSSv3 de 9.8 (Critique).

**Vulnérabilités identifiées (avec CVE) :**

*   **CVE-2025-66043 :** Débordement de tampon lorsque le Tag est 3. Une taille de données spécifiée plus grande que le buffer alloué (17 octets) permet d'écrire des données contrôlées par l'attaquant au-delà des limites du tampon `v`.
*   **CVE-2025-66044 :** Débordement de tampon lorsque le Tag est 64. Similaire à la précédente, mais affectant un tampon `tmp` de 256 octets.
*   **CVE-2025-66045 :** Débordement de tampon lorsque le Tag est 65. L'écriture de données au-delà du tampon `buf` est possible.
*   **CVE-2025-66046 :** Débordement de tampon lorsque le Tag est 67. L'écriture de données au-delà de l'entier `skew` est possible, permettant une exploitation avec des tailles de données plus petites.
*   **CVE-2025-66047 :** Débordement de tampon lorsque le Tag est 131. L'écriture de données au-delà du tampon `buf` est possible.
*   **CVE-2025-66048 :** Débordement de tampon lorsque le Tag est 133. L'écriture de données au-delà du tampon `buf` est possible.

**Recommandations :**

Il est fortement recommandé de mettre à jour la bibliothèque libbiosig vers une version patchée par le vendeur. Les utilisateurs de logiciels qui intègrent cette bibliothèque devraient également s'assurer que leurs applications utilisent la version corrigée.

---
[Source](https://talosintelligence.com/vulnerability_reports/TALOS-2025-2296){:target="_blank"}
