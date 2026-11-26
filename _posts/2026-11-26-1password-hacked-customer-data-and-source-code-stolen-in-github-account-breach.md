---
title: '1Password Hacked, Customer Data and Source Code Stolen in GitHub Account Breach'
date: 2026-11-26
permalink: /posts/2026/11/26/1password-hacked-customer-data-and-source-code-stolen-in-github-account-breach/
tags:
- veille-cyber
- hackernews
---
### Violation de sécurité chez 1Password : compromission d'un compte GitHub

1Password a récemment subi une intrusion sur son infrastructure backend suite à la compromission du compte GitHub d'un employé. Bien que des données administratives aient été dérobées, l'entreprise confirme que les coffres-forts des utilisateurs, les mots de passe et les clés de chiffrement restent inviolés.

**Points clés :**
* **Origine :** Accès non autorisé via le compte GitHub d'un collaborateur le 19 novembre 2026.
* **Impact :** Exfiltration de données clients (noms, emails, identifiants, paramètres SRP, métadonnées non secrètes) et accès au code source ainsi qu'au système CI/CD.
* **Intégrité :** Aucune donnée confidentielle (secrets ou coffres) n'a été exposée, car 1Password n'a pas accès aux clés de chiffrement de ses utilisateurs.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, l'incident résultant d'un accès illégitime aux identifiants d'un compte professionnel (compromission de compte GitHub).

**Recommandations :**
* **Pour l'entreprise :** 1Password a révoqué le jeton compromis, renforcé les contrôles sur les terminaux et le pipeline CI/CD, et durci la sécurité des emails de récupération en passant les codes de 6 chiffres à 10 caractères.
* **Pour les utilisateurs :** Aucune action immédiate n'est requise. Toutefois, une vigilance accrue est recommandée face aux tentatives potentielles de phishing utilisant les données d'identification dérobées.

---
[Source](https://thehackernews.com/2026/11/1password-hacked-customer-data-and.html){:target="_blank"}
