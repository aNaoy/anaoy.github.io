---
title: 'Accenture confirms breach after hacker offers stolen data for sale'
date: 2026-07-08
permalink: /posts/2026/07/08/accenture-confirms-breach-after-hacker-offers-stolen-data-for-sale/
tags:
- veille-cyber
- bleepingcomp
---
### Violation de données chez Accenture : fuite de code source massif

Accenture a confirmé avoir subi une intrusion informatique après qu'un acteur malveillant, identifié sous le pseudonyme « 888 », a mis en vente 35 Go de données internes sur un forum spécialisé. Bien que l'entreprise affirme que l'incident est circonscrit et n'impacte pas ses opérations, les détails de l'exfiltration soulèvent des préoccupations majeures concernant la sécurité de ses actifs numériques.

**Points clés :**
*   **Données compromises :** Le pirate prétend détenir des codes sources, des clés RSA et SSH, des jetons d'accès personnel Azure (PAT), des clés de stockage Azure et divers fichiers de configuration.
*   **Origine de l'accès :** Aucune précision n'a été apportée par Accenture sur le vecteur d'attaque ou l'implication potentielle de données clients.
*   **Historique :** Ce n'est pas la première fois qu'Accenture est visé ; le groupe a déjà été la cible du ransomware LockBit en 2021 et d'une autre fuite de données liées à ses employés en 2024.

**Vulnérabilités :**
*   Le vecteur d'attaque précis n'a pas été officiellement identifié par Accenture, et aucune CVE spécifique n'a été associée à cette intrusion. Toutefois, la nature des éléments dérobés (clés SSH, tokens Azure, configurations) pointe vers une possible compromission de la chaîne d'approvisionnement logicielle ou des environnements DevOps.

**Recommandations :**
*   **Rotation immédiate des secrets :** Renouveler en urgence toutes les clés RSA/SSH, les jetons d'accès Azure (PAT) et les clés de stockage, en supposant qu'ils sont désormais compromis.
*   **Audit des accès :** Examiner les journaux d'accès aux dépôts de code (Azure DevOps) pour identifier des accès non autorisés et révoquer tout privilège suspect.
*   **Renforcement du contrôle d'accès :** Imposer une authentification multifacteur (MFA) renforcée sur l'ensemble des plateformes de développement et limiter l'accès aux dépôts sensibles via le principe du moindre privilège.
*   **Surveillance proactive :** Mettre en œuvre des solutions de détection de fuites de données pour surveiller si des segments du code source ou des identifiants fuient sur des dépôts publics ou des plateformes de revente.

---
[Source](https://www.bleepingcomputer.com/news/security/accenture-confirms-breach-after-hacker-offers-stolen-data-for-sale/){:target="_blank"}
