---
title: 'VECT: Ransomware by design, Wiper by accident'
date: 2026-04-28
permalink: /posts/2026/04/28/vect-ransomware-by-design-wiper-by-accident/
tags:
- veille-cyber
- zerodaysfans
---
### VECT : Un Ransomware qui se comporte comme un destructeur de données

Le ransomware VECT (v2.0) est une menace multiplateforme ciblant Windows, Linux et VMware ESXi. Bien qu'il soit présenté comme un outil de chiffrement sophistiqué, une analyse révèle qu'il s'agit techniquement d'un "wiper" (destructeur de données) accidentel.

#### Points clés
*   **Destruction irrécupérable :** Le chiffrement repose sur l'algorithme ChaCha20-IETF. Pour les fichiers de plus de 128 Ko, le malware génère quatre nonces aléatoires pour quatre blocs distincts, mais n'enregistre que le dernier sur le disque. Les trois premiers sont perdus, rendant le déchiffrement impossible, même pour les attaquants.
*   **Infrastructure amateur :** Malgré une façade professionnelle (partenariats, panneau de contrôle), le code contient de graves erreurs : des modes de chiffrement ignorés, des fonctions d'anti-analyse non implémentées, et une gestion multithread inefficace.
*   **Partenariats douteux :** Le groupe collabore avec "TeamPCP" (connu pour des attaques sur la chaîne d'approvisionnement) et propose un modèle d'affiliation ouvert via BreachForums.

#### Vulnérabilités identifiées
*   **Erreur de logique de chiffrement (No CVE) :** La gestion défaillante des nonces (12 octets) lors du traitement par blocs provoque la suppression définitive des données (seuils > 131 072 octets).
*   **Absence d'authentification :** Utilisation de *ChaCha20-IETF* "brut" sans mécanisme d'intégrité (type Poly1305), rendant le chiffrement vulnérable à des manipulations.
*   **Code inachevé :** Présence de routines de sécurité compilées mais jamais appelées (code mort) et erreurs de manipulation de chaînes (double XOR).

#### Recommandations
1.  **Sauvegardes immuables :** Étant donné que le ransomware détruit les données au lieu de les chiffrer, les solutions de sauvegarde hors ligne ou immuables sont les seules protections efficaces.
2.  **Surveillance des logs :** Surveiller les exécutions de commandes système suspectes (`esxcli`, `vssadmin`, `bcdedit`) et les suppressions massives de journaux (`/var/log/*`).
3.  **Filtrage réseau et accès :** Restreindre les mouvements latéraux (SSH, PowerShell, WMI) que le malware utilise pour se propager.
4.  **Gestion des droits :** Appliquer le principe du moindre privilège, particulièrement sur les hyperviseurs ESXi, pour limiter l'impact des scripts d'arrêt de services et de VMs intégrés au ransomware.
5.  **Ne pas payer :** Le paiement ne permettra en aucun cas la récupération des données pour les fichiers dépassant 128 Ko, car les clés nécessaires (nonces) n'existent plus.

---
[Source](https://research.checkpoint.com/2026/vect-ransomware-by-design-wiper-by-accident/){:target="_blank"}
