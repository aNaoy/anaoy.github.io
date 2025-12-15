---
title: 'FreePBX Patches Critical SQLi, File-Upload, and AUTHTYPE Bypass Flaws Enabling RCE'
date: 2025-12-15
permalink: /posts/2025/12/15/freepbx-patches-critical-sqli-file-upload-and-authtype-bypass-flaws-enabling-rce/
tags:
- veille-cyber
- hackernews
---
**FreePBX : Corrections de failles critiques ouvrant la porte à l'exécution de code à distance**

Des vulnérabilités importantes ont été corrigées dans la plateforme PBX open-source FreePBX. Celles-ci incluent des injections SQL, un téléversement de fichiers arbitraire et une contournement d'authentification potentiellement critique.

**Points Clés et Vulnérabilités :**

*   **CVE-2025-61675 (Score CVSS: 8.6)** : Multiples vulnérabilités d'injection SQL (SQLi) affectant quatre points d'accès et onze paramètres. Permet une lecture et écriture sur la base de données SQL sous-jacente.
*   **CVE-2025-61678 (Score CVSS: 8.6)** : Vulnérabilité de téléversement arbitraire de fichiers (file upload) permettant à un attaquant d'injecter un web shell PHP et d'exécuter des commandes pour lire des fichiers sensibles (ex: `/etc/passwd`). Nécessite un PHPSESSID valide.
*   **CVE-2025-66039 (Score CVSS: 9.3)** : Vulnérabilité de contournement d'authentification (AUTHTYPE bypass) lorsque le type d'authentification est configuré sur "webserver". Permet à un attaquant de se connecter au panneau d'administration via un en-tête d'autorisation falsifié. Cette faille n'est pas présente dans la configuration par défaut et nécessite des réglages spécifiques dans les paramètres avancés.

Ces failles peuvent être exploitées par des attaquants pour obtenir l'exécution de code à distance (RCE) sur les instances FreePBX vulnérables.

**Recommandations :**

*   Appliquer les mises à jour de sécurité disponibles :
    *   Pour CVE-2025-61675 et CVE-2025-61678 : versions 16.0.92 et 17.0.6 (corrigé le 14 octobre 2025).
    *   Pour CVE-2025-66039 : versions 16.0.44 et 17.0.23 (corrigé le 9 décembre 2025).
*   **Mitigations temporaires recommandées** :
    *   Configurer le "Authorization Type" sur "usermanager".
    *   Définir "Override Readonly Settings" sur "No".
    *   Appliquer la nouvelle configuration et redémarrer le système.
*   Vérifier attentivement le système à la recherche de compromissions si le type d'authentification "webserver" était activé.
*   Il est fortement déconseillé d'utiliser le type d'authentification "webserver", car il est considéré comme du code hérité potentiellement moins sécurisé. Il est recommandé de le définir manuellement via la ligne de commande (`fwconsole`).

---
[Source](https://thehackernews.com/2025/12/freepbx-authentication-bypass-exposed.html){:target="_blank"}
