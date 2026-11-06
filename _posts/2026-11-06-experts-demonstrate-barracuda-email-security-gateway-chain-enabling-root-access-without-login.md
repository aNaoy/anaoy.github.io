---
title: 'Experts Demonstrate Barracuda Email Security Gateway Chain Enabling Root Access Without Login'
date: 2026-11-06
permalink: /posts/2026/11/06/experts-demonstrate-barracuda-email-security-gateway-chain-enabling-root-access-without-login/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique sur les passerelles Barracuda : accès root sans authentification

Une chaîne d'exploitation critique permet à un attaquant non authentifié d'obtenir un accès `root` complet sur les passerelles de sécurité e-mail (Email Security Gateway) de Barracuda. Cette vulnérabilité repose sur la combinaison de deux failles distinctes.

**Points clés :**
*   **Mécanisme d'attaque :** La première faille permet de contourner l'authentification pour restaurer une configuration forgée. La seconde permet d'injecter des commandes shell s'exécutant avec des privilèges `root`.
*   **Vecteur d'accès :** L'attaquant peut falsifier une somme de contrôle (checksum) de sauvegarde grâce à une clé secrète codée en dur dans le logiciel, rendant la manipulation indétectable par les contrôles standards.
*   **État de la menace :** Aucune exploitation active dans la nature n'a été signalée à ce jour, et les failles ne figurent pas encore dans le catalogue KEV de la CISA.

**Vulnérabilités identifiées :**
*   **CVE-2026-116606 (Score 9.3) :** Contournement d'autorisation permettant de modifier les paramètres globaux via une restauration de sauvegarde.
*   **CVE-2026-111560 (Score 8.6) :** Injection de commandes permettant une exécution de code à distance avec les privilèges `root`.

**Recommandations :**
*   **Mise à jour immédiate :** Installer les derniers firmwares fournis par Barracuda (version 9.4.0.030 ou supérieure pour Email Security Gateway).
*   **Sécurisation de l'accès :** En cas d'impossibilité de mettre à jour le système, restreindre l'accès à l'interface d'administration aux réseaux internes de confiance uniquement.
*   **Automatisation :** Activer les mises à jour automatiques si elles ont été précédemment désactivées.

---
[Source](https://thehackernews.com/2026/11/experts-demonstrate-barracuda-email.html){:target="_blank"}
