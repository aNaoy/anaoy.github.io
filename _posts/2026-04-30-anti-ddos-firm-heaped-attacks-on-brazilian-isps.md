---
title: 'Anti-DDoS Firm Heaped Attacks on Brazilian ISPs'
date: 2026-04-30
permalink: /posts/2026/04/30/anti-ddos-firm-heaped-attacks-on-brazilian-isps/
tags:
- veille-cyber
- krebs
---
### Détournement d'infrastructure : Une firme de cybersécurité au cœur d'un botnet au Brésil

Une enquête a révélé que **Huge Networks**, une entreprise brésilienne spécialisée dans la protection anti-DDoS, a vu ses infrastructures et les clés SSH de son PDG détournées pour orchestrer des attaques par déni de service distribué (DDoS) contre des fournisseurs d'accès internet (FAI) locaux. Le PDG, Erick Nascimento, affirme avoir été victime d'une intrusion informatique et pointe du doigt une manœuvre de déstabilisation orchestrée par un concurrent.

**Points clés :**
* **Botnet par procuration :** L'entreprise a été utilisée à son insu pour gérer un botnet massif, principalement composé de routeurs TP-Link infectés par une variante du malware **Mirai**.
* **Méthodologie :** Les attaquants exploitaient la vulnérabilité des serveurs DNS mal configurés pour lancer des attaques par réflexion et amplification, maximisant ainsi l'impact sur les cibles brésiliennes.
* **Preuves :** Des archives exposées publiquement contenaient des scripts Python malveillants et des clés d'authentification SSH privées appartenant au dirigeant de la firme.
* **Défense de l'entreprise :** Bien que des serveurs de développement aient été compromis, la direction assure avoir réagi rapidement en janvier 2026 en détruisant les machines affectées et en révoquant les accès.

**Vulnérabilités identifiées :**
* **CVE-2023-1389 :** Vulnérabilité d'injection de commande non authentifiée affectant les routeurs **TP-Link Archer AX21**, permettant aux attaquants de prendre le contrôle total des appareils pour les intégrer au botnet.

**Recommandations :**
* **Mise à jour des équipements :** Appliquer immédiatement les correctifs de sécurité fournis par les constructeurs (notamment pour la CVE-2023-1389 sur les routeurs TP-Link).
* **Sécurisation DNS :** Configurer les serveurs DNS pour restreindre les requêtes aux domaines autorisés et prévenir leur exploitation dans des attaques par réflexion.
* **Gestion des accès :** Appliquer strictement le principe du moindre privilège, sécuriser les serveurs "bastion" (jump servers) et procéder à une rotation régulière et rapide des clés SSH en cas de suspicion de compromission.
* **Audit et surveillance :** Surveiller activement les logs de sortie des serveurs pour détecter des activités anormales (scanning massif, requêtes vers des domaines C2 connus) et auditer les accès distants.

---
[Source](https://krebsonsecurity.com/2026/04/anti-ddos-firm-heaped-attacks-on-brazilian-isps/){:target="_blank"}
