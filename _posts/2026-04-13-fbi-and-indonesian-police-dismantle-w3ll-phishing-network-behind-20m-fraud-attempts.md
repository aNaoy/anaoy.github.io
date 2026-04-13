---
title: 'FBI and Indonesian Police Dismantle W3LL Phishing Network Behind $20M Fraud Attempts'
date: 2026-04-13
permalink: /posts/2026/04/13/fbi-and-indonesian-police-dismantle-w3ll-phishing-network-behind-20m-fraud-attempts/
tags:
- veille-cyber
- hackernews
---
### Démantèlement du réseau de phishing « W3LL » : Une opération d’envergure internationale

Le FBI et la police indonésienne ont neutralisé l’infrastructure de « W3LL », une plateforme de cybercriminalité « clé en main » responsable de tentatives de fraude estimées à plus de 20 millions de dollars. Le développeur présumé, identifié comme G.L., a été arrêté et les domaines clés du réseau ont été saisis.

**Points clés :**
*   **Modèle économique :** W3LL fonctionnait comme un service complet proposant des outils de phishing, des listes de diffusion et l'accès à des serveurs compromis, le tout pour environ 500 dollars.
*   **Envergure :** Actif depuis 2017, le réseau a facilité la vente de plus de 25 000 accès compromis entre 2019 et 2023. Entre 2023 et 2024, il a ciblé plus de 17 000 victimes supplémentaires via une distribution décentralisée sur des messageries chiffrées.
*   **Technique d'attaque :** La plateforme se spécialisait dans le détournement de comptes Microsoft 365.

**Vulnérabilités exploitées :**
*   **Adversary-in-the-Middle (AitM) :** Utilisation de proxys de phishing pour intercepter les sessions en temps réel.
*   **Contournement de l'authentification multi-facteurs (MFA) :** En volant les jetons de session (session cookies) via l'AitM, les attaquants s'affranchissaient des barrières MFA classiques.
*   *Note : Aucune CVE spécifique n'est associée à cet outil, car il repose sur une technique de manipulation humaine et de détournement de session plutôt que sur l'exploitation d'une faille logicielle isolée.*

**Recommandations :**
*   **Adoption de méthodes MFA résistantes au phishing :** Privilégier les clés de sécurité matérielles (FIDO2/WebAuthn) qui ne peuvent pas être interceptées par des attaques AitM, contrairement aux codes SMS ou aux applications d'authentification basées sur TOTP.
*   **Surveillance des jetons de session :** Mettre en place des politiques d'accès conditionnel strictes pour détecter et invalider les jetons de session suspects ou provenant d'adresses IP inhabituelles.
*   **Sensibilisation accrue :** Former les utilisateurs à la vérification systématique des URL avant la saisie d'identifiants, les kits de type W3LL reproduisant parfaitement l'apparence des pages de connexion légitimes.

---
[Source](https://thehackernews.com/2026/04/fbi-and-indonesian-police-dismantle.html){:target="_blank"}
