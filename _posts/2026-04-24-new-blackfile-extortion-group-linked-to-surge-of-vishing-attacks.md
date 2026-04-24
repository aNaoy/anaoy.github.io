---
title: 'New BlackFile extortion group linked to surge of vishing attacks'
date: 2026-04-24
permalink: /posts/2026/04/24/new-blackfile-extortion-group-linked-to-surge-of-vishing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### BlackFile : Vague d'extorsion par ingénierie sociale dans les secteurs du commerce et de l'hôtellerie

Le groupe cybercriminel BlackFile (aussi identifié sous les noms UNC6671, Cordial Spider ou CL-CRI-1116) mène depuis février 2026 une campagne d'extorsion ciblée. Le groupe utilise des techniques de "vishing" (phishing vocal) pour usurper l'identité du support informatique et dérober des identifiants et jetons MFA.

**Points clés :**
*   **Méthodologie :** Les attaquants contactent les employés via des numéros VoIP usurpés pour les diriger vers de fausses pages de connexion.
*   **Escalade des privilèges :** Une fois les accès compromis, les attaquants enregistrent leurs propres terminaux pour contourner le MFA, accèdent à des annuaires internes et ciblent des comptes à hauts privilèges.
*   **Exfiltration :** Exploitation des API Salesforce et des fonctions de téléchargement SharePoint pour siphonner des données confidentielles (fichiers marqués "confidentiel", numéros de sécurité sociale).
*   **Pression :** Utilisation de tactiques de "swatting" (fausses alertes aux forces de l'ordre) pour intimider les victimes après la publication des données volées sur leur site de fuite.
*   **Connexions :** Présence de liens probables avec le réseau cybercriminel "The Com".

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée ; l'attaque repose sur l'exploitation de **l'ingénierie sociale (facteur humain)** et l'abus de fonctionnalités légitimes (API Salesforce/SharePoint) pour contourner les contrôles de sécurité standard.

**Recommandations :**
*   **Renforcement des procédures :** Établir des protocoles stricts de vérification d'identité pour toute demande d'assistance technique, incluant une authentification multifacteur robuste pour les appels.
*   **Formation :** Organiser des exercices de simulation d'ingénierie sociale ciblés pour le personnel en première ligne.
*   **Surveillance :** Surveiller étroitement les accès aux API de type SaaS et les comportements anormaux lors des sessions SSO authentifiées pour détecter les exfiltrations massives.

---
[Source](https://www.bleepingcomputer.com/news/security/new-blackfile-extortion-gang-targets-retail-and-hospitality-orgs/){:target="_blank"}
