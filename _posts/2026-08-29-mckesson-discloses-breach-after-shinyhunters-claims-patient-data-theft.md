---
title: 'McKesson discloses breach after ShinyHunters claims patient data theft'
date: 2026-08-29
permalink: /posts/2026/08/29/mckesson-discloses-breach-after-shinyhunters-claims-patient-data-theft/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque majeure contre McKesson : le groupe ShinyHunters mis en cause

Le géant de la distribution pharmaceutique McKesson a été victime d’une violation de données impliquant des accès non autorisés à des applications tierces. Le groupe de cybercriminels ShinyHunters revendique le vol de 284 millions d'enregistrements de données patients et réclame une rançon de plus de 55 millions de dollars.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de l'ingénierie sociale via le "vishing" (phishing vocal). Les attaquants ont usurpé l'identité du support technique via des domaines trompeurs (ex: `mckesson[.]claims`).
*   **Compromission :** Les assaillants ont compromis des comptes Okta (SSO) pour accéder aux environnements Salesforce et Snowflake.
*   **Volume de données :** Environ 1 To de données exfiltrées entre le 21 et le 25 août 2026. Le chiffre de 284 millions correspond au nombre total d'enregistrements (lignes), et non au nombre unique de patients.
*   **Nature des données :** Informations personnelles identifiables (noms, adresses, numéros de sécurité sociale), dossiers médicaux, ordonnances, données sur les prestataires de santé et communications internes.
*   **Réponse :** McKesson a activé ses protocoles d'incident et mène une enquête en collaboration avec des experts, sans avoir pour l'heure cédé à la demande de rançon.

**Vulnérabilités :**
Aucune CVE spécifique n'est citée. La faille repose sur une vulnérabilité humaine (ingénierie sociale) et sur l'exploitation de comptes d'accès légitimes (Single Sign-On).

**Recommandations :**
*   **Renforcement de l'authentification :** Implémenter une authentification multifacteur (MFA) résistante au phishing (clés matérielles FIDO2/WebAuthn) plutôt que des méthodes basées sur les SMS ou les notifications push.
*   **Sensibilisation :** Former les employés à reconnaître les tactiques de vishing et à vérifier systématiquement l'authenticité des demandes d'assistance IT.
*   **Surveillance des identités :** Surveiller étroitement les accès aux environnements SaaS et Cloud (Okta, Salesforce, Snowflake) et détecter les comportements anormaux ou les accès depuis des sources inhabituelles.
*   **Protection des domaines :** Mettre en œuvre une veille active sur les domaines malveillants utilisant le nom de la marque (typosquatting ou usurpation de services).

---
[Source](https://www.bleepingcomputer.com/news/security/mckesson-discloses-breach-after-shinyhunters-claims-patient-data-theft/){:target="_blank"}
