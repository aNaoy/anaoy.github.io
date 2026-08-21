---
title: 'Suspected Russian Hackers Abuse Google OAuth and WhatsApp Linking to Hijack Accounts'
date: 2026-08-21
permalink: /posts/2026/08/21/suspected-russian-hackers-abuse-google-oauth-and-whatsapp-linking-to-hijack-accounts/
tags:
- veille-cyber
- hackernews
---
### Campagnes d'espionnage russe : détournement des flux d'authentification et compromission Wi-Fi

Des groupes de cyberespionnage russes (UNC6293, UNC7005 et UNC5976) mènent des campagnes ciblées contre le milieu universitaire, l'aérospatiale, la défense et les gouvernements en Europe et aux États-Unis. Ces attaquants exploitent des fonctionnalités d'authentification légitimes pour détourner des comptes et exfiltrer des données.

#### Points clés
*   **Tactiques diversifiées :** Utilisation intensive du phishing par OAuth, de mots de passe d'application spécifiques et du détournement de codes de couplage d'appareils (notamment sur WhatsApp et Microsoft Entra ID).
*   **Infrastructure "CaptiveCrunch" :** Compromission de routeurs Wi-Fi publics (hôtels, aéroports) via une possible attaque sur la chaîne d'approvisionnement des prestataires de services managés (MSP). Les attaquants utilisent le détournement DNS pour rediriger les victimes vers des portails de phishing.
*   **Malwares avancés :** Déploiement de chevaux de Troie comme *CornFlake* (RAT) et *ChocoShell* (PowerShell) pour l'exfiltration de jetons de session, de mots de passe et la surveillance audio/vidéo.
*   **Ciblage :** Approches ultra-sélectives avec des thèmes diplomatiques, des invitations à des conférences ou des leurres liés au soutien à l'Ukraine.

#### Vulnérabilités exploitées
*   **Abus de flux OAuth :** Détournement des jetons d'authentification via des applications cloud malveillantes.
*   **Détournement DNS (DNS Poisoning) :** Manipulation des passerelles Wi-Fi pour forcer le trafic vers des infrastructures de type "Adversary-in-the-Middle" (AitM).
*   **Device Code Phishing :** Exploitation du flux d'authentification par code de couplage pour usurper l'identité de l'utilisateur sur des plateformes légitimes.
*   *Note : Aucune CVE spécifique n'est mentionnée, les attaques reposant sur le détournement de fonctionnalités légitimes et l'ingénierie sociale.*

#### Recommandations
*   **Renforcement de l'authentification :** Privilégier les clés de sécurité physiques (FIDO2) plutôt que les méthodes basées sur les codes SMS ou les applications de couplage d'appareils, plus vulnérables au phishing AitM.
*   **Surveillance des accès MSP :** Les organisations doivent auditer les accès distants accordés à leurs prestataires de services informatiques et limiter les privilèges au strict nécessaire.
*   **Sécurisation Wi-Fi :** Utiliser systématiquement un VPN chiffré lors de l'utilisation de réseaux Wi-Fi publics.
*   **Analyse des permissions OAuth :** Réviser régulièrement les autorisations accordées aux applications tierces connectées aux comptes Google et Microsoft.
*   **Vigilance sur les leurres :** Sensibiliser le personnel aux tactiques de spear-phishing personnalisées (invitations à des sommets, liens vers des partages de fichiers inhabituels).

---
[Source](https://thehackernews.com/2026/08/suspected-russian-hackers-abuse-google.html){:target="_blank"}
