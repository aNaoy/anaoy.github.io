---
title: '“Legitimate” phishing: how attackers weaponize Amazon SES to bypass email security'
date: 2026-05-04
permalink: /posts/2026/05/04/legitimate-phishing-how-attackers-weaponize-amazon-ses-to-bypass-email-security/
tags:
- veille-cyber
- securelist
---
### Détournement d'Amazon SES : Le phishing légitime

Des attaquants exploitent Amazon Simple Email Service (SES) pour mener des campagnes de phishing hautement crédibles, contournant les filtres de sécurité traditionnels en utilisant une infrastructure cloud réputée.

**Points clés**
*   **Crédibilité technique :** Les emails envoyés via Amazon SES passent avec succès les protocoles d'authentification SPF, DKIM et DMARC, et ne sont pas bloqués par les listes de réputation IP.
*   **Abus de confiance :** L'utilisation de domaines Amazon (`amazonaws.com` ou `amazonses.com`) rassure les utilisateurs, facilitant le vol d'identifiants ou la fraude au président (BEC).
*   **Techniques employées :** Les attaquants utilisent des redirections masquées, des templates HTML personnalisés et des fils de discussion factices pour tromper les destinataires.

**Vulnérabilités exploitées**
*   **Fuites de secrets AWS :** L'origine principale des attaques réside dans le vol de clés d'accès IAM, souvent exposées par erreur sur des dépôts GitHub publics, des fichiers de configuration ou des instances Docker.
*   *Note : Il ne s'agit pas d'une vulnérabilité logicielle (CVE) spécifique au service Amazon, mais d'une exploitation de mauvaises pratiques de gestion des identités et des accès (IAM).*

**Recommandations**
*   **Gestion des accès :** Appliquer le principe du moindre privilège et privilégier l'utilisation de **rôles IAM** plutôt que de clés d'accès statiques.
*   **Sécurisation des comptes :** Activer systématiquement l'authentification multifacteur (MFA), restreindre les accès par adresse IP et automatiser la rotation des clés.
*   **Audits :** Effectuer des audits de sécurité réguliers pour détecter les secrets exposés.
*   **Vigilance utilisateur :** Ne pas se fier uniquement à l'adresse de l'expéditeur ou à l'apparence du domaine. En cas de réception de documents inattendus, vérifier systématiquement la demande via un canal de communication secondaire.
*   **Protection technique :** Utiliser des solutions de sécurité mail avancées capables d'analyser le contenu des messages plutôt que de se baser uniquement sur la réputation des domaines expéditeurs.

---
[Source](https://securelist.com/amazon-ses-phishing-and-bec-attacks/119623/){:target="_blank"}
