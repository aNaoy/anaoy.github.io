---
title: 'Data analyst sent to prison for stealing data, extorting employer'
date: 2026-08-14
permalink: /posts/2026/08/14/data-analyst-sent-to-prison-for-stealing-data-extorting-employer/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation pour extorsion cybernétique : le cas Brightly Software

Un ancien analyste de données contractuel, Cameron Curry, a été condamné à deux ans de prison pour avoir tenté d'extorquer 2,5 millions de dollars à son ex-employeur, Brightly Software. Après la non-reconduction de son contrat, l'individu a utilisé ses accès aux données internes pour dérober des informations sensibles sur le personnel, puis a menacé de divulguer ces données (PII) et de dénoncer l'entreprise auprès de la SEC si une rançon en cryptomonnaie n'était pas versée.

**Points clés :**
*   **Mode opératoire :** L'auteur a exploité des accès légitimes obtenus durant sa mission pour exfiltrer des données salariales et personnelles.
*   **Escalade des menaces :** La demande initiale de rançon augmentait de 100 000 $ par mois supplémentaire de non-paiement.
*   **Intervention :** Suite au signalement de l'entreprise, le FBI a perquisitionné le domicile de l'auteur, saisissant les preuves numériques ayant permis sa condamnation.
*   **Contexte de sécurité :** L'entreprise avait déjà subi une violation de données distincte en 2023 touchant 3 millions d'utilisateurs.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, qui relève d'une **menace interne (insider threat)**. La faille principale réside dans le maintien des accès privilégiés au-delà de la fin du contrat et dans l'insuffisance des contrôles d'accès basés sur le principe du moindre privilège.

**Recommandations :**
*   **Gestion stricte des accès (IAM) :** Révocation immédiate et automatique de tous les droits d'accès dès la fin d'un contrat de travail.
*   **Surveillance des logs :** Mise en place d'une surveillance active des accès aux bases de données sensibles par le personnel interne (notamment les accès inhabituels en fin de contrat).
*   **Protection des données (DLP) :** Utilisation de solutions de prévention contre la perte de données pour détecter et bloquer l'exfiltration massive d'informations sensibles (PII).
*   **Principe du moindre privilège :** Restreindre strictement les accès aux données critiques uniquement aux employés dont les fonctions le nécessitent impérativement.

---
[Source](https://www.bleepingcomputer.com/news/security/data-analyst-sent-to-prison-for-stealing-data-extorting-employer/){:target="_blank"}
