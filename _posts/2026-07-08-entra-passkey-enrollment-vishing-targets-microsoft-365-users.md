---
title: 'Entra passkey enrollment vishing targets Microsoft 365 users'
date: 2026-07-08
permalink: /posts/2026/07/08/entra-passkey-enrollment-vishing-targets-microsoft-365-users/
tags:
- veille-cyber
- bleepingcomp
---
# Campagne de vishing ciblant l'enrôlement de passkeys Microsoft Entra

Le groupe d'extorsion « Pink » (traqué sous le nom O-UNC-066) mène une campagne de vishing (hameçonnage vocal) sophistiquée pour compromettre les comptes Microsoft 365. En se faisant passer pour le support informatique, les attaquants incitent les employés à enregistrer un « passkey » (clé d'accès) sous leur contrôle, profitant de la récente généralisation de ces outils par Microsoft.

### Points clés
*   **Mode opératoire :** L'attaquant appelle la victime et la dirige vers un portail de phishing imitant parfaitement l'interface officielle de Microsoft.
*   **Kit de phishing dynamique :** Contrairement au proxy classique, le kit est piloté en temps réel par un opérateur qui adapte le processus aux méthodes MFA de la victime (TOTP, notifications push, SMS).
*   **Technique de leurre :** Le site malveillant demande à la victime de noter une fausse phrase de récupération (BIP-39), une pratique inexistante dans le processus légitime d'Entra, utilisée pour détourner l'attention.
*   **Objectif :** Une fois le contrôle du compte obtenu, le groupe exfiltre rapidement des données sensibles depuis SharePoint et OneDrive pour faire chanter les entreprises.

### Vulnérabilités
Il n'existe pas de CVE spécifique, car il s'agit d'une **exploitation par ingénierie sociale** visant à détourner les fonctionnalités légitimes de gestion des identités (IAM) de Microsoft Entra.

### Recommandations
*   **Vérification de l'identité :** Mettre en place des protocoles stricts pour vérifier l'identité des membres du support technique lors d'interactions téléphoniques.
*   **Sensibilisation :** Informer les utilisateurs que les procédures légitimes d'enregistrement de passkey ne nécessitent jamais la saisie de phrases de récupération (seed phrases) BIP-39.
*   **Restrictions géographiques :** Bloquer les connexions et les demandes d'authentification provenant de régions géographiques où l'entreprise n'opère pas.
*   **Surveillance :** Surveiller les domaines suspects contenant des mots-clés liés à l'authentification (ex: « passkey ») et surveiller les accès inhabituels vers SharePoint et OneDrive.

---
[Source](https://www.bleepingcomputer.com/news/security/entra-passkey-enrollment-vishing-targets-microsoft-365-users/){:target="_blank"}
