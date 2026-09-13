---
title: 'Attackers Use Passkey Phishing to Hijack Microsoft Cloud Accounts and Exfiltrate Data'
date: 2026-09-13
permalink: /posts/2026/09/13/attackers-use-passkey-phishing-to-hijack-microsoft-cloud-accounts-and-exfiltrate-data/
tags:
- veille-cyber
- hackernews
---
### Campagnes de phishing Microsoft : Fraude aux factures et détournement de comptes via les passkeys

Microsoft a récemment identifié deux campagnes d'attaque majeures exploitant l'ingénierie sociale et les infrastructures légitimes pour compromettre des environnements cloud.

#### Points clés
*   **Fraude financière (BEC) :** Utilisation de l'IA générative pour créer des emails personnalisés et des factures falsifiées, se faisant passer pour des dirigeants (CEO/CFO) afin de manipuler les départements comptables vers des virements ACH frauduleux.
*   **Vol de comptes Cloud :** Utilisation de techniques d'ingénierie sociale basées sur les "passkeys" (clés d'accès). Les attaquants contactent les victimes par téléphone ou via Microsoft Teams en se faisant passer pour le support informatique, les incitant à "mettre à jour" leur configuration d'authentification sur des sites de phishing.
*   **Persistance :** Une fois l'accès obtenu, les attaquants enregistrent leur propre méthode d'authentification MFA (téléphone ou application) pour maintenir un accès permanent, puis utilisent l'API Microsoft Graph pour exfiltrer massivement des données (SharePoint, OneDrive, Exchange).

#### Vulnérabilités exploitées
*   **Techniques d'ingénierie sociale :** Ciblage humain via du "vishing" (phishing vocal) et l'usurpation d'identité pour contourner les contrôles de sécurité.
*   **Attaques Adversary-in-the-Middle (AitM) et Device-Code :** Détournement des flux d'authentification légitimes pour capturer des jetons ou forcer l'approbation d'accès.
*   **Abus de l'API Microsoft Graph :** Utilisation détournée d'outils légitimes d'administration pour la reconnaissance interne et l'exfiltration, rendant la détection difficile par les outils classiques basés sur des alertes isolées.
*   **Note :** Aucune CVE spécifique n'est mentionnée, les attaques reposant sur des abus de fonctionnalités légitimes et non sur des failles logicielles.

#### Recommandations
*   **Détection holistique :** Analyser l'activité de l'API Microsoft Graph de manière corrélée plutôt que par des appels isolés, afin de repérer les comportements anormaux (exfiltration massive, reconnaissance).
*   **Sécurisation du processus d'assistance IT :** Sensibiliser les employés au fait que le support informatique ne demandera jamais de mettre à jour une passkey via un lien envoyé par SMS ou un appel non sollicité.
*   **Gestion des accès :** Surveiller étroitement l'ajout de nouvelles méthodes MFA par les utilisateurs et appliquer des politiques de moindre privilège pour limiter l'impact en cas de compromission d'un compte.
*   **Vigilance sur l'infrastructure :** Bloquer les domaines suspects utilisés pour le phishing (ex: `passkeyhelpdesk[.]com`, `setupmypasskey[.]com`) et surveiller l'usurpation de domaines d'entreprise.

---
[Source](https://thehackernews.com/2026/09/attackers-use-passkey-phishing-to.html){:target="_blank"}
