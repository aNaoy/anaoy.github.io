---
title: 'Sality botnet infrastructure dismantled in joint global takedown'
date: 2026-09-02
permalink: /posts/2026/09/02/sality-botnet-infrastructure-dismantled-in-joint-global-takedown/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement mondial de l'infrastructure du botnet Sality

Une coalition internationale regroupant les forces de l'ordre (FBI, Europol, Eurojust, DOJ) et des partenaires privés, dont CrowdStrike, a mis fin aux activités du botnet Sality, actif depuis plus de deux décennies. L'opération a consisté à saisir des domaines clés et à mettre en œuvre une technique de « sinkhole » (trou noir) pour isoler les machines infectées et couper les canaux de communication peer-to-peer du réseau.

**Points clés :**
*   **Historique :** Actif depuis 2003, ce botnet a infecté plus de 15 000 appareils.
*   **Acteurs :** Le groupe criminel SALTY SPIDER, probablement basé dans la République de Bachkirie (Russie), était aux commandes.
*   **Méthodes d'attaque :** Historiquement utilisé pour le vol d'identifiants, le spam et les attaques DDoS, le botnet distribuait ces huit dernières années le malware **EggJagger**.
*   **Technique malveillante :** EggJagger est un outil de « clipjacking » qui surveille le presse-papier des victimes pour remplacer les adresses de portefeuilles de cryptomonnaies par celles des attaquants.

**Vulnérabilités :**
*   Le botnet reposait sur une architecture Peer-to-Peer (P2P) robuste, utilisant des « super peers » comme colonne vertébrale pour diffuser des charges utiles et des instructions de téléchargement. Aucune CVE spécifique n'est mentionnée, l'infection s'appuyant sur des vulnérabilités réseau classiques et des vecteurs de compromission persistants.

**Recommandations :**
*   **Analyse de sécurité :** Effectuer des scans complets des systèmes d'entreprise pour détecter les traces persistantes du malware Sality ou de sa charge utile EggJagger.
*   **Hygiène des actifs :** Puisque le botnet visait le remplacement d'adresses de cryptomonnaies, les utilisateurs doivent vérifier l'intégrité de leurs transactions et s'assurer que leurs outils de gestion de portefeuilles ne présentent pas d'anomalies.
*   **Protection des accès :** Renforcer la surveillance après l'accès initial, car une fois les identifiants compromis, les mesures de prévention classiques perdent en efficacité.

---
[Source](https://www.bleepingcomputer.com/news/security/sality-botnet-infrastructure-dismantled-in-joint-global-takedown/){:target="_blank"}
