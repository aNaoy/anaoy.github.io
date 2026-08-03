---
title: 'Thermo Fisher Patches Flaw That Could Make DNA File Tampering Nearly Undetectable'
date: 2026-08-03
permalink: /posts/2026/08/03/thermo-fisher-patches-flaw-that-could-make-dna-file-tampering-nearly-undetectable/
tags:
- veille-cyber
- hackernews
---
### Risque de falsification de preuves ADN : Vulnérabilité dans les logiciels Thermo Fisher

Thermo Fisher Scientific a publié un correctif pour plusieurs de ses logiciels d'identification humaine Applied Biosystems afin de corriger une vulnérabilité critique permettant la modification indétectable de fichiers de données ADN (.fsa et .hid) avant leur analyse.

**Points clés :**
*   La faille permet à un attaquant ayant un accès local ou réseau aux serveurs de laboratoire de manipuler des fichiers de profil ADN sans laisser de traces détectables par les logiciels d'analyse.
*   Des tests ont démontré qu'il est possible de fusionner des profils ADN et de créer des fichiers falsifiés semblant dater de plusieurs années.
*   Cette faiblesse potentielle pourrait affecter les enregistrements numériques générés depuis 1995.
*   Aucune preuve d'exploitation malveillante n'a été recensée à ce jour.
*   Trois gammes de produits en fin de vie (EOL) ne bénéficieront d'aucune mise à jour.

**Vulnérabilité :**
*   **CVE-2026-17583** : Score CVSS v4.0 de 8.2 (Sévérité "Élevée").

**Recommandations :**
*   **Mise à jour immédiate :** Installer les correctifs disponibles pour les cinq gammes de produits supportées. Ces mises à jour intègrent des signatures numériques permettant de vérifier l'intégrité des fichiers.
*   **Mesures compensatoires (pour les systèmes non mis à jour ou en fin de vie) :**
    *   Renforcer la chaîne de traçabilité des fichiers.
    *   Utiliser des supports de stockage chiffrés et protégés par mot de passe.
    *   Appliquer strictement le principe du moindre privilège sur les systèmes d'analyse.
    *   Restreindre la connectivité réseau aux seules sources de confiance.

---
[Source](https://thehackernews.com/2026/08/thermo-fisher-patches-flaw-that-could.html){:target="_blank"}
