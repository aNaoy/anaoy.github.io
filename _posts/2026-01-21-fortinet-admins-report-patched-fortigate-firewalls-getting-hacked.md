---
title: 'Fortinet admins report patched FortiGate firewalls getting hacked'
date: 2026-01-21
permalink: /posts/2026/01/21/fortinet-admins-report-patched-fortigate-firewalls-getting-hacked/
tags:
- veille-cyber
- bleepingcomp
---
### Contournement de Patch sur les Pare-feux FortiGate

Des administrateurs Fortinet rapportent que des attaquants exploitent une faille critique de contournement de patch sur les pare-feux FortiGate, affectant même des versions censées être corrigées. Cette vulnérabilité (CVE-2025-59718) permet des connexions non autorisées via la fonctionnalité FortiCloud SSO, menant à la création de comptes administrateurs malveillants.

**Points Clés :**

*   Des attaques réussies ont été observées sur des dispositifs fonctionnant avec FortiOS 7.4.9 et même 7.4.10.
*   Les attaquants créent des comptes administrateurs locaux en exploitant le mécanisme de connexion SSO de FortiCloud.
*   Fortinet reconnaît que la vulnérabilité persiste dans les versions récentes et prévoit de publier des mises à jour supplémentaires (7.4.11, 7.6.6, 8.0.0).
*   La faille a été ajoutée au catalogue des vulnérabilités activement exploitées par la CISA.

**Vulnérabilités :**

*   **CVE-2025-59718 :** Contournement d'authentification critique sur FortiCloud SSO. Permet à des attaquants de créer des comptes administrateurs sur les pare-feux FortiGate.

**Recommandations :**

*   **Désactiver temporairement la fonction FortiCloud SSO :** Si activée, il est conseillé de la désactiver dans les paramètres système (Système -> Paramètres -> Désactiver "Autoriser la connexion administrative via FortiCloud SSO") ou via l'interface de ligne de commande avec la commande :
    ```
    config system global
    set admin-forticloud-sso-login disable
    end
    ```
*   **Appliquer les mises à jour de FortiOS :** Dès que les nouvelles versions corrigées (7.4.11, 7.6.6, 8.0.0) seront disponibles, il sera crucial de les installer.

Il est important de noter que la fonctionnalité FortiCloud SSO n'est pas activée par défaut si le dispositif n'est pas enregistré auprès de FortiCare, ce qui limite potentiellement le nombre de systèmes exposés. Cependant, des milliers de dispositifs avec cette fonction activée restent accessibles en ligne.

---
[Source](https://www.bleepingcomputer.com/news/security/fortinet-admins-report-patched-fortigate-firewalls-getting-hacked/){:target="_blank"}
