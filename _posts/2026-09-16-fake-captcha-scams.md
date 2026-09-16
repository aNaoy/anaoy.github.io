---
title: 'Fake CAPTCHA Scams'
date: 2026-09-16
permalink: /posts/2026/09/16/fake-captcha-scams/
tags:
- veille-cyber
- schneier
---
### Menace des faux CAPTCHAs : L'ingénierie sociale au service de l'exécution de code

Les campagnes de « faux CAPTCHA » exploitent l'habitude des utilisateurs de valider des tests de sécurité pour les inciter à exécuter des commandes malveillantes sur leur système. Cette méthode, souvent répertoriée sous les noms de « ClickFix » ou « FileFix », détourne le processus de vérification pour installer des malwares.

**Points clés :**
*   **Techniques de dissimulation (TDS) :** Les attaquants utilisent des systèmes de routage sophistiqués qui analysent l'adresse IP et le profil de l'utilisateur (fingerprinting). Si la requête provient d'un centre de données ou d'un outil de scan, une page bénigne est affichée pour éviter la détection. Les cibles réelles (adresses résidentielles/mobiles) reçoivent la charge utile malveillante.
*   **Mode opératoire :** L'attaque demande à l'utilisateur d'effectuer une manipulation manuelle, comme ouvrir la boîte de dialogue « Exécuter » (Win+R) et y coller une ligne de commande PowerShell ou `pcalua.exe`.
*   **Exécution de code :** La commande force le téléchargement d'un script (ex: `.sct`) qui est ensuite exécuté via `regsvr32`, contournant ainsi les protections classiques par l'exécution de fichiers système légitimes.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle spécifique avec un identifiant CVE unique, mais plutôt d'une exploitation de l'**ingénierie sociale** couplée au détournement de composants légitimes de Windows (Living-off-the-Land) tels que :
    *   `pcalua.exe` (Program Compatibility Assistant)
    *   `regsvr32.exe` (outil d'enregistrement de composants COM)
    *   `curl.exe` (pour le téléchargement de la charge utile)

**Recommandations :**
*   **Vigilance comportementale :** Aucun CAPTCHA légitime ne demande jamais de copier-coller du texte dans une console, d'exécuter des commandes système ou de télécharger des exécutables.
*   **Formation des utilisateurs :** Sensibiliser au fait qu'une vérification humaine doit rester une interaction simple sur le navigateur (clics ou sélection d'images).
*   **Fermeture immédiate :** En cas de demande suspecte sur une page web, fermez immédiatement l'onglet ou le navigateur sans suivre les instructions affichées.
*   **Filtrage réseau :** Surveiller les communications sortantes vers des services de type `sslip.io` ou des domaines suspects utilisés pour héberger des scripts de test.

---
[Source](https://www.schneier.com/blog/archives/2026/09/fake-captcha-scams.html){:target="_blank"}
