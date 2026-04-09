---
title: 'Google: New UNC6783 hackers steal corporate Zendesk support tickets'
date: 2026-04-09
permalink: /posts/2026/04/09/google-new-unc6783-hackers-steal-corporate-zendesk-support-tickets/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'extorsion par le groupe UNC6783 ciblant les prestataires BPO

Le groupe de cybercriminels UNC6783, potentiellement lié à l'entité « Raccoon », mène une campagne d'envergure visant des prestataires de services externalisés (BPO) pour infiltrer de grandes entreprises. L'objectif est l'exfiltration de données sensibles pour des demandes d'extorsion.

**Points clés :**
* **Cibles :** Prestataires BPO et grandes entreprises multisectorielles.
* **Mode opératoire :** Utilisation intensive de l'ingénierie sociale (phishing) et de chats en direct pour piéger le personnel de support.
* **Technique de contournement MFA :** Déploiement de kits de phishing capturant le contenu du presse-papier pour intercepter les sessions MFA et enregistrer les appareils des attaquants.
* **Vecteurs secondaires :** Distribution de fausses mises à jour de sécurité contenant des chevaux de Troie d'accès distant (RAT).
* **Impact :** Vol massif de données, incluant des tickets de support client, des documents internes et des dossiers d'employés.

**Vulnérabilités exploitées :**
* Absence de CVE spécifique mentionnée ; les attaques reposent sur des failles humaines et le contournement des méthodes MFA traditionnelles via des pages de connexion Okta falsifiées (domaines de type `[org].zendesk-support[##].com`).

**Recommandations de sécurité :**
* **Authentification forte :** Déployer des clés de sécurité matérielles basées sur le standard FIDO2, insensibles aux techniques de phishing classiques.
* **Surveillance proactive :** Auditer régulièrement les appareils enregistrés dans les systèmes MFA et surveiller les sessions de chat en direct pour détecter des comportements anormaux.
* **Filtrage réseau :** Bloquer les domaines imitant les patterns de support Zendesk.
* **Sensibilisation :** Renforcer la formation du personnel de helpdesk face aux tentatives d'ingénierie sociale ciblée.

---
[Source](https://www.bleepingcomputer.com/news/security/google-new-unc6783-hackers-steal-corporate-zendesk-support-tickets/){:target="_blank"}
