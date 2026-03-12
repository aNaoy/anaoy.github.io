---
title: '“Handala Hack” – Unveiling Group’s Modus Operandi'
date: 2026-03-12
permalink: /posts/2026/03/12/handala-hack-unveiling-groups-modus-operandi/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse de la menace : Le groupe "Handala Hack" (Void Manticore)

**Handala Hack** est un acteur de menace affilié au ministère iranien du Renseignement et de la Sécurité (MOIS), également connu sous les noms de Void Manticore, Red Sandstorm ou Banished Kitten. Le groupe mène des opérations destructrices ("wiper") et des campagnes de "hack and leak", principalement contre Israël, l'Albanie et, plus récemment, des entreprises américaines.

#### Points clés
*   **Mode opératoire :** Le groupe privilégie une approche manuelle ("hands-on") dans les réseaux compromis.
*   **Stratégie de destruction :** Les attaquants déploient simultanément plusieurs méthodes de destruction pour maximiser les dommages, utilisant des outils légitimes (VeraCrypt) et des scripts personnalisés (parfois assistés par IA).
*   **Persistance et latéralisation :** Utilisation intensive du RDP et déploiement de l'outil **NetBird** pour créer des réseaux maillés (zero-trust) permettant de tunneler le trafic et de maintenir des points d'accès internes.
*   **Évolution :** Après une période de discipline opérationnelle, le groupe montre un relâchement sécuritaire, utilisant parfois directement des adresses IP iraniennes ou des connexions via Starlink.

#### Vulnérabilités et techniques exploitées
Bien qu'aucune CVE spécifique ne soit citée, l'attaquant exploite des faiblesses structurelles et des vecteurs connus :
*   **Accès initial :** Attaques par force brute sur les infrastructures VPN et utilisation d'identifiants compromis.
*   **Élévation de privilèges :** Extraction de secrets via `LSASS` (via `comsvcs.dll` et `rundll32.exe`) et export de ruches de registre (`HKLM`).
*   **Reconnaissance :** Utilisation d'outils comme `ADRecon` pour énumérer l'Active Directory.
*   **Distribution malveillante :** Utilisation des stratégies de groupe (GPO) pour diffuser des scripts de connexion et exécuter des charges utiles destructrices à distance.

#### Recommandations de sécurité
*   **Authentification :** Imposer l'authentification multifacteur (MFA) pour tous les accès distants et comptes à hauts privilèges.
*   **Surveillance :** Détecter les anomalies de connexion (horaires atypiques, échecs répétés suivis d'un succès, nouvelles IP provenant de fournisseurs type VPN/hosting ou Starlink).
*   **Gestion des accès :** 
    *   Restreindre ou interdire le RDP s'il n'est pas strictement nécessaire ; surveiller les noms d'hôtes par défaut (`DESKTOP-XXXXXX`).
    *   Filtrer les connexions provenant de zones géographiques à haut risque.
*   **Durcissement :** Surveiller l'installation d'outils de gestion à distance non autorisés (RMM) et de logiciels de tunneling comme **NetBird**.
*   **Politique réseau :** Restreindre temporairement l'accès VPN aux pays strictement nécessaires aux activités professionnelles.

---
[Source](https://research.checkpoint.com/2026/handala-hack-unveiling-groups-modus-operandi/){:target="_blank"}
