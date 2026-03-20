---
title: 'Ex-data analyst stole company data in $2.5M extortion scheme'
date: 2026-03-20
permalink: /posts/2026/03/20/ex-data-analyst-stole-company-data-in-25m-extortion-scheme/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation pour extorsion : un ancien prestataire détourne les données de son entreprise

Un ancien analyste de données contractuel, Cameron Curry, a été reconnu coupable d'avoir extorqué son ex-employeur, la société Brightly Software. Suite à la non-reconduction de son contrat, il a utilisé ses accès privilégiés pour voler des informations confidentielles, dont les données personnelles (PII) des employés, afin de faire chanter l'entreprise pour un montant de 2,5 millions de dollars.

**Points clés :**
* **Mode opératoire :** Curry a exfiltré des documents sensibles entre août et décembre 2023. Après la fin de son contrat, il a adressé plus de 60 e-mails de menaces, assortis de preuves de possession des données, exigeant une rançon sous peine de fuite publique et de dénonciation auprès de la SEC.
* **Résultat :** L'entreprise a initialement versé 7 540 $ en Bitcoin avant de contacter le FBI. L'enquête a mené à l'arrestation de Curry et à la saisie de ses appareils. Il risque désormais jusqu'à 12 ans de prison.
* **Contexte :** Brightly Software avait déjà été victime d'une violation de données distincte en avril 2023, affectant 3 millions d'utilisateurs de sa plateforme SchoolDude.

**Vulnérabilités :**
* Cet incident ne repose pas sur une vulnérabilité logicielle (CVE), mais sur une **vulnérabilité interne liée aux accès privilégiés (Insider Threat)**. L'absence de révocation immédiate ou de contrôle strict des droits d'accès après la fin du contrat a permis l'exfiltration.

**Recommandations :**
* **Gestion des accès (IAM) :** Appliquer strictement le principe du moindre privilège et automatiser la révocation immédiate des accès lors de la fin de contrat d'un prestataire.
* **Surveillance des données (DLP) :** Déployer des solutions de prévention contre la perte de données pour détecter et bloquer l'exfiltration massive de fichiers sensibles.
* **Politique de départ :** Renforcer les procédures de sécurité lors du "offboarding" des employés et contractuels, incluant la supervision des sessions critiques en fin de mission.
* **Réponse aux incidents :** Impliquer immédiatement les autorités compétentes (FBI/Police) en cas de chantage, plutôt que de céder à la demande de rançon.

---
[Source](https://www.bleepingcomputer.com/news/security/data-analyst-found-guilty-of-extorting-brightly-software-of-25-million/){:target="_blank"}
