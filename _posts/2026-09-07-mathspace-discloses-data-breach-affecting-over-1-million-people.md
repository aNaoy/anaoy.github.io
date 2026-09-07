---
title: 'Mathspace discloses data breach affecting over 1 million people'
date: 2026-09-07
permalink: /posts/2026/09/07/mathspace-discloses-data-breach-affecting-over-1-million-people/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données massive chez Mathspace : 1 million d'utilisateurs impactés

La plateforme d'apprentissage en ligne Mathspace a subi une intrusion majeure compromettant les données personnelles de 1 079 819 personnes (élèves, parents et personnel éducatif) en Australie et en Nouvelle-Zélande. L'incident, attribué au groupe de cybercriminels *ShinyHunters*, s'inscrit dans une campagne mondiale visant les instances vulnérables du logiciel de reporting Metabase.

**Points clés :**
*   **Période de l'incident :** Accès initial le 10 août 2026, exfiltration des données le 27 août 2026, confirmation de la brèche le 3 septembre 2026.
*   **Données exposées :** Informations personnelles identifiables (noms, emails, liens potentiels avec des établissements scolaires).
*   **Ce qui n'a pas été compromis :** Les mots de passe (hashs), les résultats scolaires, les dossiers d'évaluation, les jetons d'authentification (SSO) et les clés API sont restés sécurisés.
*   **Contexte :** Cette attaque fait partie d'une vague d'exploitations visant des entreprises utilisant des instances auto-hébergées de Metabase, incluant d'autres victimes comme Framework et Tally.

**Vulnérabilités :**
*   **Exploitation d'une vulnérabilité critique :** Les attaquants ont exploité une faille de type **injection SQL** (Zero-day) dans l'installation auto-hébergée de Metabase. Cette faille a permis aux assaillants d'obtenir des privilèges d'administrateur sans nécessiter d'identifiants légitimes. (Bien que non explicitement nommée dans le texte, cette série d'attaques sur Metabase est généralement associée à la vulnérabilité **CVE-2023-38646**).

**Recommandations pour les utilisateurs :**
*   **Vigilance accrue :** Rester à l'affût d'activités suspectes sur les comptes (tentatives de connexion inhabituelles, notifications de réinitialisation de mot de passe non sollicitées).
*   **Protection contre le phishing :** Les données volées pourraient être utilisées pour mener des campagnes d'ingénierie sociale ciblées. La prudence est requise face aux communications suspectes utilisant ces informations personnelles.

---
[Source](https://www.bleepingcomputer.com/news/security/mathspace-discloses-data-breach-affecting-over-1-million-people/){:target="_blank"}
