---
title: 'Fortinet warns of critical FortiCloud SSO login auth bypass flaws'
date: 2025-12-09
permalink: /posts/2025/12/09/fortinet-warns-of-critical-forticloud-sso-login-auth-bypass-flaws/
tags:
- veille-cyber
- bleepingcomp
---
**Alertes de Sécurité Fortinet : Failles Critiques dans l'Authentification SSO FortiCloud**

Fortinet a publié des mises à jour pour corriger deux vulnérabilités critiques affectant FortiOS, FortiWeb, FortiProxy et FortiSwitchManager. Ces failles permettent aux attaquants de contourner l'authentification SSO FortiCloud en exploitant des faiblesses dans la vérification des signatures cryptographiques via des messages SAML malveillants.

**Points Clés :**

*   **Vulnérabilités critiques :** Deux failles permettent un contournement de l'authentification SSO FortiCloud.
*   **Produits affectés :** FortiOS, FortiWeb, FortiProxy, FortiSwitchManager.
*   **Mécanisme d'attaque :** Exploitation via des messages SAML malveillants abusant d'une mauvaise vérification des signatures cryptographiques.
*   **Activation par défaut :** La fonctionnalité SSO FortiCloud n'est pas activée par défaut, sauf si l'appareil est enregistré auprès de FortiCare et que l'option "Allow administrative login using FortiCloud SSO" n'est pas désactivée lors de l'enregistrement.

**Vulnérabilités identifiées :**

*   **CVE-2025-59718 :** Affecte FortiOS, FortiProxy, FortiSwitchManager.
*   **CVE-2025-59719 :** Affecte FortiWeb.

**Recommandations :**

*   **Mise à jour des systèmes :** Appliquer les mises à jour de sécurité fournies par Fortinet pour les produits concernés.
*   **Désactivation temporaire :** Si une mise à jour n'est pas immédiatement possible, désactiver temporairement la fonctionnalité de connexion FortiCloud SSO. Cela peut être fait via l'interface graphique (System -> Settings -> "Allow administrative login using FortiCloud SSO" désactivé) ou via la ligne de commande :
    ```
    config system global
    set admin-forticloud-sso-login disable
    end
    ```

L'article mentionne également d'autres vulnérabilités corrigées récemment par Fortinet, notamment une faille de modification de mot de passe non vérifiée (CVE-2025-59808) et une autre permettant l'authentification par hachage de mot de passe (CVE-2025-64471). Les produits Fortinet sont fréquemment ciblés par des attaques sophistiquées.

---
[Source](https://www.bleepingcomputer.com/news/security/fortinet-warns-of-critical-forticloud-sso-login-auth-bypass-flaws/){:target="_blank"}
