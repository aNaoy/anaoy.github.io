---
title: 'Factoring RSA Keys with Many Zeros'
date: 2026-06-29
permalink: /posts/2026/06/29/factoring-rsa-keys-with-many-zeros/
tags:
- veille-cyber
- schneier
---
### Vulnérabilité des clés RSA présentant des motifs de zéros répétitifs

Des recherches récentes menées par le projet *badkeys* ont identifié une nouvelle catégorie de clés RSA fragilisées, caractérisées par des motifs de blocs de zéros régulièrement espacés. Ces clés, détectées dans des logs de transparence de certificats (CT), des services SSH et des clés PGP, s'avèrent vulnérables à des techniques de factorisation polynomiale, permettant de retrouver les facteurs premiers du module RSA.

**Points clés :**
* **Origine des données :** L'analyse repose sur un large échantillon de clés collectées via des scans TLS/SSH et des logs CT.
* **Impact identifié :** Des certificats utilisés par de grandes entreprises (Yahoo, Verizon) et des équipements (NetApp) présentaient ces motifs.
* **Logiciels concernés :** Le logiciel *CompleteFTP* est explicitement mis en cause pour la génération de clés RSA (v10.0.0-12.0.0) et DSA (v10.0.0-23.0.4) défectueuses.
* **Hypothèse de backdoor :** La nature systématique de ces erreurs dans diverses implémentations indépendantes soulève la possibilité d'une porte dérobée délibérément insérée dans les processus de génération de clés.

**Vulnérabilités :**
* Bien qu'aucune CVE spécifique ne soit assignée dans l'article, la vulnérabilité réside dans une implémentation logicielle défaillante lors de la génération de nombres premiers, créant des structures "creuses" prévisibles dans le module RSA.

**Recommandations :**
* **Audit des clés :** Utiliser des outils d'analyse de clés publiques (comme *badkeys*) pour identifier les modules RSA présentant des motifs de zéros atypiques.
* **Mise à jour logicielle :** S'assurer que les systèmes générant des clés cryptographiques utilisent des bibliothèques de cryptographie à jour et conformes aux standards actuels (génération aléatoire robuste).
* **Renouvellement :** Révoquer et remplacer systématiquement toute clé identifiée comme présentant ces motifs de sparsité.

---
[Source](https://www.schneier.com/blog/archives/2026/06/factoring-rsa-keys-with-many-zeros.html){:target="_blank"}
