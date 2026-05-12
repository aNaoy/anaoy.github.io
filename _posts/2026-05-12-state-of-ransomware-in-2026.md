---
title: 'State of ransomware in 2026'
date: 2026-05-12
permalink: /posts/2026/05/12/state-of-ransomware-in-2026/
tags:
- veille-cyber
- securelist
---
### État de la menace ransomware en 2026 : Évolutions et stratégies de défense

En 2026, le paysage du ransomware se transforme : bien que le nombre d'organisations touchées soit en légère baisse, la menace reste critique en raison d'une professionnalisation accrue des acteurs et d'une diversification des méthodes d'extorsion.

#### Points clés
*   **Diversification des tactiques :** Les attaquants privilégient désormais l'extorsion sans chiffrement (« encryptionless extortion »), se concentrant sur le vol et la menace de divulgation de données.
*   **Chiffrement post-quantique :** Apparition de familles de ransomwares (ex: PE32 utilisant l'algorithme Kyber1024) capables de résister aux futures capacités de calcul quantique, rendant le déchiffrement sans clé impossible.
*   **Neutralisation des défenses :** Utilisation massive d'« EDR killers » et de la technique **BYOVD** (Bring Your Own Vulnerable Driver) pour désactiver les solutions de sécurité avant l'exécution de la charge utile.
*   **Industrialisation de l'accès :** Les courtiers en accès initial (IAB) privilégient désormais les portails **RDWeb** comme vecteur privilégié, profitant de la sécurisation accrue des accès RDP classiques.
*   **Modèle opérationnel :** Le marché évolue vers le « Ransomware-as-a-Service » (RaaS) avec des groupes hautement structurés (Qilin, Clop, Akira) et des nouveaux entrants (The Gentlemen) adoptant des approches très ciblées et professionnelles.

#### Vulnérabilités et vecteurs d'attaque
*   **Vecteurs d'entrée :** Exploitation récurrente de RDWeb, VPN et appareils réseau (FortiOS, SonicWall, Cisco ASA).
*   **BYOVD (Bring Your Own Vulnerable Driver) :** Exploitation de pilotes légitimes signés mais vulnérables pour contourner les protections EDR.
*   **Logiciels non mis à jour :** Persistance de l'exploitation de failles connues non patchées sur des systèmes critiques.

#### Recommandations de sécurité
*   **Gestion des accès :**
    *   Proscrire l'exposition directe d'interfaces d'administration (RDP, RDWeb) sur Internet ; utiliser systématiquement un VPN ou une solution ZTNA.
    *   Appliquer strictement le principe du moindre privilège (PoLP) et généraliser l'authentification multifacteur (MFA).
    *   Réaliser des audits réguliers des ports ouverts et des permissions.
*   **Renforcement technique :**
    *   Activer les listes de blocage des pilotes vulnérables (ex: *Microsoft Vulnerable Driver Blocklist*).
    *   Déployer des solutions EDR/XDR capables de détecter le chargement de pilotes suspects ou la terminaison forcée de processus de sécurité.
    *   Segmenter le réseau pour limiter les mouvements latéraux des attaquants.
*   **Résilience organisationnelle :**
    *   Maintenir des sauvegardes immuables et hors ligne (air-gapped), testées régulièrement.
    *   Former les employés à la détection de campagnes de phishing, y compris celles assistées par IA.
    *   Ne jamais payer les rançons : l'incertitude sur la récupération des données et le financement du crime organisé rendent cette option non viable.

---
[Source](https://securelist.com/state-of-ransomware-in-2026/119761/){:target="_blank"}
