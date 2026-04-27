---
title: 'Home security giant ADT data breach affects 5.5 million people'
date: 2026-04-27
permalink: /posts/2026/04/27/home-security-giant-adt-data-breach-affects-55-million-people/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite de données massive chez ADT : 5,5 millions de clients exposés

Le géant de la sécurité domestique ADT a subi une intrusion informatique majeure, confirmée par le service *Have I Been Pwned*. Le groupe de cybercriminels ShinyHunters a exfiltré et publié sur le dark web une archive de 11 Go contenant les données personnelles de 5,5 millions d'individus après le refus de l'entreprise de céder à une tentative d'extorsion.

**Points clés :**
* **Nature de l'attaque :** Vol de données via une compromission de compte professionnel.
* **Volume :** 5,5 millions de dossiers clients impactés.
* **Données compromises :** Noms, numéros de téléphone, adresses physiques, adresses e-mail, dates de naissance et, pour une partie des victimes, les quatre derniers chiffres des numéros de sécurité sociale ou numéros fiscaux.
* **Limites de l'incident :** Aucune information de paiement (bancaire/carte de crédit) n'a été dérobée et les systèmes de sécurité des clients sont restés intacts.
* **Contexte :** Il s'agit du troisième incident de sécurité majeur pour ADT en moins d'un an.

**Vulnérabilités exploitées :**
* L'attaque a été rendue possible par une campagne de **vishing** (phishing vocal) visant un employé d'ADT.
* Les attaquants ont compromis un compte de connexion unique (**SSO Okta**) pour accéder à l'instance Salesforce de l'entreprise.
* Aucune CVE spécifique n'est mentionnée, l'attaque reposant sur l'ingénierie sociale et l'abus d'accès légitimes (Identity-based attack).

**Recommandations :**
* **Renforcement de l'authentification :** Implémenter une authentification multifacteur (MFA) résistante au phishing (clés matérielles FIDO2/WebAuthn) pour tous les accès SSO et SaaS.
* **Formation à la cybersécurité :** Sensibiliser les employés aux tactiques de vishing pour prévenir l'usurpation d'identifiants.
* **Gestion des accès :** Appliquer le principe du moindre privilège sur les plateformes SaaS (Salesforce, Microsoft 365, etc.) pour limiter l'impact d'une compromission de compte unique.
* **Surveillance :** Renforcer la détection d'anomalies sur les accès aux bases de données et aux outils de gestion de la relation client (CRM).

---
[Source](https://www.bleepingcomputer.com/news/security/home-security-giant-adt-data-breach-affects-55-million-people/){:target="_blank"}
