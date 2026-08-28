---
title: '19 Chrome and Edge Extensions Found With Wallet-Stealing and Crypto-Draining Code'
date: 2026-08-28
permalink: /posts/2026/08/28/19-chrome-and-edge-extensions-found-with-wallet-stealing-and-crypto-draining-code/
tags:
- veille-cyber
- hackernews
---
### Vague de malwares dans les extensions Chrome et Edge : la campagne "Superior"

Des chercheurs en cybersécurité ont identifié 19 extensions pour Google Chrome et Microsoft Edge, actives depuis février 2024, conçues pour voler des identifiants et drainer des fonds en cryptomonnaies. Cette campagne, baptisée "Superior", repose sur une technique de compromission sophistiquée : les attaquants achètent des extensions légitimes existantes ou publient des versions saines, pour ensuite déployer une mise à jour malveillante via le système de mise à jour automatique des navigateurs.

**Points clés :**
*   **Mode opératoire :** Les extensions agissent en double usage : elles conservent leurs fonctionnalités initiales tout en communiquant avec un serveur de commande et contrôle (C2) pour recevoir des instructions et exécuter du code arbitraire.
*   **Infrastructure dynamique :** Les attaquants utilisent une rotation d'adresses C2 pour segmenter les victimes et échapper à la détection.
*   **Techniques d'exfiltration :** Le code injecté supprime les politiques de sécurité (CSP) des pages visitées et déploie 16 modules malveillants, incluant des outils de vol de portefeuilles, de récupération de phrases de récupération (seed phrases), ainsi que des intercepteurs de formulaires et de réseaux sociaux (Facebook, LinkedIn).
*   **Impact :** L'extension "Enable Right Click & Copy" a atteint à elle seule 80 000 installations.

**Vulnérabilités :**
Aucune CVE spécifique n'est associée, car il s'agit d'un usage détourné des mécanismes de mise à jour légitimes et de l'injection de scripts via les permissions accordées par les extensions. L'exploitation repose sur le contournement des Content Security Policy (CSP).

**Recommandations :**
*   **Audit des extensions :** Passer en revue les extensions installées et supprimer celles qui ne sont plus nécessaires ou dont la source semble douteuse (notamment les outils SEO, convertisseurs crypto ou utilitaires de productivité).
*   **Désactivation des mises à jour automatiques (si possible) :** Bien que difficile pour un usage grand public, une vigilance accrue est requise lors des mises à jour d'extensions.
*   **Vigilance face aux faux messages :** Se méfier des invitations de type "ClickFix" (fausses mises à jour de navigateur) demandant de copier-coller des commandes dans un terminal.
*   **Protection des actifs :** Ne jamais stocker de phrases de récupération ou de clés privées dans le navigateur et privilégier les solutions de stockage à froid (hardware wallets).

---
[Source](https://thehackernews.com/2026/08/19-chrome-and-edge-extensions-found.html){:target="_blank"}
