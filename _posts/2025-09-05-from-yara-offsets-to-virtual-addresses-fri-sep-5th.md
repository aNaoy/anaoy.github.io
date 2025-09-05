---
title: 'From YARA Offsets to Virtual Addresses, (Fri, Sep 5th)'
date: 2025-09-05
permalink: /posts/2025/09/05/from-yara-offsets-to-virtual-addresses-fri-sep-5th/
tags:
- veille-cyber
- sans-isc
---
**Analyse de Code Malware : Du Fichier à la Mémoire Vive**

Cet article détaille une méthode permettant de localiser des séquences d'octets identifiées par YARA dans un fichier exécutable, afin de les retrouver dans un environnement de débogage ou de désassemblage.

**Points Clés :**

*   YARA est un outil puissant pour la recherche de motifs binaires dans les fichiers.
*   L'option "-s" de YARA permet d'afficher les décalages (offsets) dans le fichier où les motifs sont trouvés.
*   Pour analyser ces motifs dans un débogueur, il est nécessaire de convertir les décalages bruts du fichier en adresses virtuelles dans la mémoire du processus.
*   Cela implique de comprendre la structure du format PE (Portable Executable), notamment les sections et leurs adresses virtuelles (RVA et VA).

**Vulnérabilités :**

Aucune vulnérabilité spécifique n'est mentionnée ou exploitée dans cet article. L'objectif est l'analyse de code potentiellement malveillant, et non l'exploitation de failles.

**Recommandations :**

*   Utiliser YARA avec l'option "-s" pour obtenir les décalages de fichiers des motifs identifiés.
*   Analyser la structure des sections d'un fichier PE (via des outils comme `pefile` en Python) pour connaître leurs décalages et adresses virtuelles.
*   Appliquer une formule de conversion pour passer du décalage de fichier à l'adresse virtuelle relative (RVA), puis à l'adresse virtuelle absolue (VA) en utilisant l'ImageBase du fichier PE.
*   Utiliser un script dédié (comme celui mentionné, disponible sur GitHub) pour automatiser ce processus de mappage.
*   Une fois l'adresse virtuelle déterminée, utiliser un débogueur ou un désassembleur pour examiner le code et évaluer sa nature malveillante.

---
[Source](https://isc.sans.edu/diary/rss/32262){:target="_blank"}
