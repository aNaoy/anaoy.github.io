---
title: 'Fake CAPTCHA Scams'
date: 2026-09-16
permalink: /posts/2026/09/16/fake-captcha-scams/
tags:
- veille-cyber
- schneier
---
### La menace des faux CAPTCHAs : techniques et vecteurs d'attaque

Les campagnes de « faux CAPTCHA » (notamment identifiées sous les noms « ClickFix » ou « FileFix ») exploitent la confiance des utilisateurs envers les outils de vérification humaine pour orchestrer des compromissions de systèmes.

**Points clés :**
*   **Technique d'ingénierie sociale :** L'utilisateur est invité à effectuer une manipulation complexe (ex: `Win+R` suivi d'une commande) sous prétexte de valider une vérification de sécurité.
*   **Détection évasive :** Les attaquants utilisent des *Traffic Direction Systems* (TDS) pour filtrer les connexions. Les adresses IP liées aux centres de données (utilisées par les outils d'analyse de menaces) reçoivent des pages bénignes, tandis que les IP résidentielles ou mobiles reçoivent la charge utile malveillante.
*   **Exécution de code :** La manipulation demandée déclenche généralement l'exécution de `pcalua.exe` pour télécharger et exécuter des scripts distants (fichiers `.sct`) via `regsvr32`.

**Vulnérabilités exploitées :**
*   L'attaque n'exploite pas une faille logicielle spécifique (CVE), mais abuse de fonctionnalités natives du système d'exploitation Windows (Living-off-the-Land) comme `pcalua.exe` et `regsvr32.exe` pour exécuter du code arbitraire avec l'autorisation de l'utilisateur.

**Recommandations :**
*   **Vigilance comportementale :** Aucun CAPTCHA légitime ne demande à un utilisateur de copier-coller des commandes dans un terminal, de télécharger un logiciel ou de manipuler des fonctions système (`Win+R`).
*   **Fermeture immédiate :** En cas de demande suspecte de manipulation système sur une page web, fermez immédiatement le navigateur sans exécuter les instructions.
*   **Filtrage réseau :** Être conscient que les attaquants ciblent préférentiellement les réseaux résidentiels pour éviter la détection par les outils de sécurité automatisés.

---
[Source](https://www.schneier.com/blog/archives/2026/09/fake-captcha-scams.html){:target="_blank"}
