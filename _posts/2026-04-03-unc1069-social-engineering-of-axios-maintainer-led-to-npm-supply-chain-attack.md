---
title: 'UNC1069 Social Engineering of Axios Maintainer Led to npm Supply Chain Attack'
date: 2026-04-03
permalink: /posts/2026/04/03/unc1069-social-engineering-of-axios-maintainer-led-to-npm-supply-chain-attack/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement npm : L'attaque ciblée contre Axios

Le responsable du projet Axios, Jason Saayman, a été victime d'une campagne d'ingénierie sociale sophistiquée menée par le groupe nord-coréen **UNC1069**. Cette attaque a permis d'introduire des versions malveillantes du package (1.14.1 et 0.30.4) contenant l'implant **WAVESHAPER.V2**.

**Points clés :**
*   **Mode opératoire :** Les attaquants ont usurpé l'identité d'un fondateur d'entreprise légitime et ont invité le mainteneur dans un espace Slack factice très crédible.
*   **Technique d'infection :** Lors d'un appel vidéo via Microsoft Teams, un faux message d'erreur système a incité le mainteneur à exécuter une mise à jour malveillante, déclenchant le déploiement d'un cheval de Troie d'accès distant (RAT).
*   **Impact :** Une fois le système compromis, les attaquants ont dérobé les identifiants npm pour publier des versions empoisonnées du package. Le malware utilisé, **SilentSiphon**, permet le vol massif de secrets (GitHub, npm, pip, etc.) et de données de navigation.
*   **Portée :** Avec près de 100 millions de téléchargements hebdomadaires, la compromission d'Axios expose une vaste partie de l'écosystème JavaScript par le biais des dépendances directes et transitives.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais souligne l'exploitation de vecteurs de type **ClickFix** (pop-ups trompeurs incitant à exécuter des scripts PowerShell ou AppleScript malveillants).

**Recommandations pour les mainteneurs :**
*   **Sécurisation des accès :** Adopter les flux OIDC (*OpenID Connect*) pour la publication de paquets afin d'éviter l'usage de tokens statiques.
*   **Durcissement des processus :** Mettre en place des versions immuables et suivre les bonnes pratiques pour les GitHub Actions.
*   **Hygiène de sécurité :** Réinitialiser systématiquement les appareils et l'ensemble des identifiants en cas de doute sur une compromission.
*   **Vigilance :** Se méfier des demandes de support ou de collaboration imprévues, même si elles semblent provenir de sources professionnelles crédibles.

---
[Source](https://thehackernews.com/2026/04/unc1069-social-engineering-of-axios.html){:target="_blank"}
