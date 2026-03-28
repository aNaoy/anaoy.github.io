---
title: 'Iran-Linked Hackers Breach FBI Director’s Personal Email, Hit Stryker With Wiper Attack'
date: 2026-03-28
permalink: /posts/2026/03/28/iran-linked-hackers-breach-fbi-directors-personal-email-hit-stryker-with-wiper-attack/
tags:
- veille-cyber
- hackernews
---
### Escalade des cyberattaques iraniennes : piratages ciblés et opérations de destruction

Le groupe de hackers « Handala », affilié au ministère iranien du Renseignement (MOIS), a intensifié ses activités malveillantes en visant des cibles américaines stratégiques, dont le piratage de la messagerie personnelle du directeur du FBI, Kash Patel, et une cyberattaque destructrice par « wiper » contre la firme Stryker. Cette offensive s'inscrit dans un contexte de tensions géopolitiques accrues, le groupe délaissant l'espionnage pur au profit d'opérations psychologiques et de sabotage.

**Points clés :**
* **Changement de paradigme :** Handala, également connu sous les noms de Banished Kitten ou Void Manticore, multiplie les attaques destructrices contre des entreprises du Fortune 500 pour maximiser l'impact psychologique.
* **Complexité tactique :** Les attaquants utilisent des outils légitimes (VeraCrypt pour chiffrer les disques, RDP pour le mouvement latéral) et s'appuient sur l'infrastructure criminelle (infostealers, Telegram pour le C2) pour masquer leur origine et rendre l'attribution difficile.
* **Infiltration de la supply chain :** Les attaquants exploitent les identités numériques et les accès aux systèmes de gestion d'endpoints comme Microsoft Intune.
* **Riposte américaine :** Le ministère de la Justice a saisi quatre domaines utilisés par le MOIS pour des opérations de déstabilisation et a émis une prime de 10 millions de dollars pour tout renseignement sur le groupe.

**Vulnérabilités exploitées :**
* **Compromission d'identifiants :** Utilisation d'identifiants volés via des logiciels malveillants de type "infostealer".
* **Exploitation de services d'administration :** Phishing ciblé et détournement des accès administrateur via Microsoft Intune.
* **Accès VPN :** Usage récurrent de comptes VPN compromis pour l'accès initial au réseau.
*(Note : Aucune CVE spécifique n'a été mentionnée dans l'article, les attaques reposant sur des abus d'accès légitimes et du social engineering).*

**Recommandations de sécurité :**
* **Gestion des accès :** Appliquer strictement le principe du moindre privilège pour tous les comptes administratifs.
* **Authentification forte :** Imposer une authentification multifacteur (MFA) résistante au phishing.
* **Durcissement des systèmes :** Activer la validation par plusieurs administrateurs (« multi-admin approval ») pour toute modification sensible dans les outils de gestion comme Microsoft Intune.
* **Surveillance accrue :** Surveiller les comportements anormaux liés aux scripts de connexion (Group Policy) et aux outils de chiffrement de disque déployés de manière non autorisée.

---
[Source](https://thehackernews.com/2026/03/iran-linked-hackers-breach-fbi.html){:target="_blank"}
