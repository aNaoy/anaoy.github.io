---
title: 'SmartApeSG campaign uses ClickFix page to push Remcos RAT, (Sat, Mar 14th)'
date: 2026-03-14
permalink: /posts/2026/03/14/smartapesg-campaign-uses-clickfix-page-to-push-remcos-rat-sat-mar-14th/
tags:
- veille-cyber
- sans-isc
---
### Propagation de Remcos RAT via la campagne SmartApeSG

La campagne « SmartApeSG » exploite des sites web légitimes compromis pour déployer le cheval de Troie d'accès à distance (RAT) Remcos. L'attaque utilise une technique d'ingénierie sociale dite « ClickFix », consistant à afficher une fausse page CAPTCHA incitant l'utilisateur à copier-coller un script malveillant dans la fenêtre « Exécuter » de Windows.

**Points clés :**
*   **Vecteur d'infection :** Injection de scripts malveillants sur des sites web vulnérables.
*   **Méthode de compromission :** Tromperie via une fausse vérification humaine (CAPTCHA) demandant l'exécution manuelle d'une commande système.
*   **Déploiement :** Une fois la commande exécutée, le malware est téléchargé sous forme d'archive ZIP (déguisée en fichier `.pdf`).
*   **Persistance :** Utilisation de la technique de *DLL side-loading* et modification du registre Windows.

**Vulnérabilités :**
*   Cette attaque ne repose pas sur une faille logicielle spécifique (CVE), mais sur une vulnérabilité humaine : l'exécution volontaire de commandes par l'utilisateur (ingénierie sociale). Le processus tire profit de la confiance accordée aux sites compromis et de la manipulation des fonctionnalités natives de Windows.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à ne jamais copier-coller ou exécuter des commandes provenant de sites web, même en réponse à des messages d'erreur ou des vérifications de sécurité.
*   **Contrôle des accès :** Restreindre l'accès à la fenêtre « Exécuter » ou limiter les droits d'exécution de scripts PowerShell/CMD via des politiques de groupe (GPO).
*   **Sécurité périmétrique :** Bloquer les connexions vers les domaines suspects identifiés dans la chaîne d'infection et surveiller les communications TLS sortantes vers des adresses IP inconnues.
*   **Protection des endpoints :** Utiliser des solutions EDR pour détecter les comportements suspects, notamment le *DLL side-loading* et les modifications persistantes dans le registre Windows.

---
[Source](https://isc.sans.edu/diary/rss/32796){:target="_blank"}
