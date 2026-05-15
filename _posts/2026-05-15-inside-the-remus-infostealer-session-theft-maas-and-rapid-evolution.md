---
title: 'Inside the REMUS Infostealer: Session Theft, MaaS, and Rapid Evolution'
date: 2026-05-15
permalink: /posts/2026/05/15/inside-the-remus-infostealer-session-theft-maas-and-rapid-evolution/
tags:
- veille-cyber
- bleepingcomp
---
### REMUS : L’Évolution Professionnelle des Infostealers en Mode MaaS

REMUS est un nouveau logiciel malveillant de type *infostealer* (voleur d'informations) qui a rapidement évolué grâce à un modèle économique de "Malware-as-a-Service" (MaaS). Analysé entre février et mai 2026, ce logiciel se distingue non seulement par ses capacités techniques — héritées en partie du *Lumma Stealer* — mais surtout par la structuration quasi professionnelle de son exploitation commerciale.

**Points clés :**
*   **Modèle MaaS structuré :** Les opérateurs traitent le développement du logiciel comme une entreprise légitime, avec des cycles de mise à jour rapides, un support client 24/7, et une amélioration constante de l'interface utilisateur.
*   **Priorité au vol de session :** Le malware délaisse le simple vol de mots de passe au profit de la capture de cookies et de jetons d'authentification. L'objectif est de contourner les systèmes d'authentification multifacteur (MFA) en utilisant des sessions déjà actives.
*   **Ciblage des gestionnaires de mots de passe :** Des fonctionnalités ont été ajoutées pour extraire des données depuis les extensions de gestionnaires populaires comme 1Password, LastPass et Bitwarden, ainsi que via le stockage local IndexedDB.
*   **Maturité opérationnelle :** La plateforme offre désormais des outils de gestion de campagne avancés (tableaux de bord statistiques, suivi des "travailleurs", filtrage des logs en double).

**Vulnérabilités exploitées :**
*   L'article ne mentionne pas de CVE spécifique, mais souligne l'exploitation des mécanismes de stockage des navigateurs (IndexedDB) et des jetons de session persistants. Le malware utilise des techniques anti-VM et des méthodes de contournement du chiffrement des navigateurs.

**Recommandations :**
*   **Surveillance des sessions :** Étant donné que les cookies et les jetons de session permettent de contourner la MFA, il est crucial de surveiller activement les expositions de ces données sur le dark web et via les canaux Telegram.
*   **Gestion des accès :** Implémenter des politiques de durée de vie de session plus courtes et une détection des accès inhabituels (utilisation de proxys SOCKS5 suspects).
*   **Sécurisation des endpoints :** Maintenir des solutions EDR (Endpoint Detection and Response) capables de détecter les comportements suspects liés à l'exécution de loaders et à l'accès illicite aux fichiers de stockage des navigateurs et des extensions de mots de passe.

---
[Source](https://www.bleepingcomputer.com/news/security/inside-the-remus-infostealer-session-theft-maas-and-rapid-evolution/){:target="_blank"}
