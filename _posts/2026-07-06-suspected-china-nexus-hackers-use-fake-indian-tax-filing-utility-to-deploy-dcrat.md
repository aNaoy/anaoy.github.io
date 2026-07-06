---
title: 'Suspected China-Nexus Hackers Use Fake Indian Tax Filing Utility to Deploy DcRAT'
date: 2026-07-06
permalink: /posts/2026/07/06/suspected-china-nexus-hackers-use-fake-indian-tax-filing-utility-to-deploy-dcrat/
tags:
- veille-cyber
- hackernews
---
### Opération DragonReturn : Espionnage ciblé via de faux utilitaires fiscaux

Une campagne d'espionnage sophistiquée, baptisée **Operation DragonReturn**, cible les contribuables et les professionnels de la finance en Inde. Les attaquants, probablement liés à des groupes basés en Chine (avec des similitudes tactiques avec le groupe *Silver Fox*), utilisent des e-mails de hameçonnage usurpant l'identité du département de l'impôt sur le revenu indien pour distribuer le cheval de Troie d'accès distant **DcRAT**.

**Points clés :**
*   **Vecteur d'attaque :** E-mails de phishing incitant à télécharger un utilitaire de déclaration fiscale factice via un lien malveillant.
*   **Techniques de dissimulation :** Utilisation du *DLL sideloading* pour charger des charges utiles cachées dans des fichiers images (fichiers JPG convertis en conteneurs de DLL).
*   **Persistance :** Création d'un service Windows nommé « MixedSvc » pour un accès à long terme.
*   **Objectifs :** Vol de données sensibles, exfiltration d'informations et prise de contrôle totale des machines.
*   **Anti-analyse :** Le malware détecte les environnements de sandbox et désactive les analyses AMSI (Antimalware Scan Interface).

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée ; l'attaque repose sur l'ingénierie sociale et des techniques de contournement légitimes, telles que le *DLL sideloading* et l'élévation de privilèges via UAC (*User Account Control*).

**Recommandations :**
*   **Vigilance sur les sources :** Ne téléchargez jamais d'utilitaires, de logiciels ou de formulaires fiscaux en dehors des portails gouvernementaux officiels.
*   **Analyse des liens :** Vérifiez systématiquement les URL avant de cliquer. Méfiez-vous des domaines suspects imitant des services officiels (ex: `govtop[.]one`).
*   **Contrôle des privilèges :** Restreignez les droits d'administration sur les postes de travail pour limiter l'impact des installations non autorisées.
*   **Sécurité des e-mails :** Sensibilisez les équipes financières aux campagnes de phishing saisonnières exploitant les périodes de déclaration fiscale.
*   **Surveillance réseau :** Bloquez les connexions vers les domaines et adresses IP identifiés comme C2 (notamment `204.194.48[.]250` et `kkxqbh[.]top`).

---
[Source](https://thehackernews.com/2026/07/suspected-china-nexus-hackers-use-fake.html){:target="_blank"}
