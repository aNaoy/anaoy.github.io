---
title: 'China-Aligned Groups Ramp Up Attacks: Dragon Weave Hits Czech Republic & Taiwan'
date: 2026-06-01
permalink: /posts/2026/06/01/china-aligned-groups-ramp-up-attacks-dragon-weave-hits-czech-republic-taiwan/
tags:
- veille-cyber
- hackernews
---
### Intensification des campagnes d'espionnage cybernétique liées à la Chine

Des groupes de cyberespionnage alignés sur les intérêts chinois multiplient leurs attaques mondiales, notamment à travers l'opération « Dragon Weave ». Cette campagne cible des entités gouvernementales, académiques et financières en République tchèque et à Taïwan via des courriels de spear-phishing contenant des archives ZIP malveillantes.

**Points clés :**
*   **Méthodes d'infection :** Utilisation de fichiers LNK factices ou de binaires Rust pour exécuter des scripts PowerShell ou des chargeurs (RUSTCLOAK).
*   **Technique de persistance :** Recours systématique au *DLL side-loading* pour exécuter des charges utiles dissimulées.
*   **C2 furtif :** La campagne Dragon Weave utilise « AZUREVEIL », un agent exploitant le stockage Microsoft Azure Blob pour échanger des données via une approche « dead drop », évitant ainsi la communication directe avec un serveur pirate.
*   **Diversification :** D'autres outils et groupes (TencShell, PhiliKit, NegativeGlimmer) ont été identifiés, ciblant des infrastructures critiques dans 37 pays, avec une préférence pour les secteurs technologiques stratégiques.

**Vulnérabilités exploitées :**
*   **DLL Side-loading :** Technique détournant le chargement légitime de bibliothèques (ex: `UnityPlayer.dll`) pour injecter du code malveillant.
*   **Aucune CVE spécifique n'est mentionnée** dans cet article ; les attaquants privilégient l'ingénierie sociale et le détournement de services cloud légitimes plutôt que l'exploitation de vulnérabilités logicielles connues.

**Recommandations :**
*   **Filtrage des emails :** Renforcer les contrôles sur les pièces jointes, particulièrement les fichiers compressés (ZIP) contenant des raccourcis (LNK) ou des exécutables suspects.
*   **Surveillance du trafic Cloud :** Surveiller les accès inhabituels ou persistants vers les conteneurs de stockage cloud (comme Azure Blob Storage) qui pourraient servir de vecteurs de communication C2.
*   **Endpoint Detection (EDR) :** Déployer des solutions capables de détecter le *DLL side-loading* et l'exécution de scripts PowerShell non autorisés.
*   **Sensibilisation :** Alerter le personnel sur les risques liés à l'ouverture de documents provenant de sources non vérifiées, même lorsqu'ils se présentent sous des formats bureautiques courants.

---
[Source](https://thehackernews.com/2026/06/china-aligned-groups-ramp-up-attacks.html){:target="_blank"}
