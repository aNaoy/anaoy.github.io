---
title: 'Hackers breach Fortinet FortiGate devices, steal firewall configs'
date: 2026-01-22
permalink: /posts/2026/01/22/hackers-breach-fortinet-fortigate-devices-steal-firewall-configs/
tags:
- veille-cyber
- bleepingcomp
---
## Attaques sur des appareils FortiGate : Compromission et Vol de Configurations

Des attaques automatisées ciblent actuellement des dispositifs Fortinet FortiGate. Ces attaques visent à créer des comptes non autorisés et à subtiliser des données de configuration de pare-feu. La campagne a débuté le 15 janvier, exploitant une vulnérabilité inconnue dans la fonctionnalité de connexion unique (SSO) de ces appareils.

Ces incidents rappellent des attaques similaires documentées en décembre, exploitant une faille critique de contournement d'authentification (CVE-2025-59718). Cette vulnérabilité permettait à des attaquants non authentifiés de contourner le SSO via des messages SAML malveillants, lorsque les fonctions SSO FortiCloud étaient activées. Bien que des correctifs aient été publiés, des rapports récents indiquent que des administrateurs de Fortinet voient leurs pare-feu, même patchés, être compromis, suggérant une possible contournement de ces correctifs. La dernière version de FortiOS (7.4.10) ne semble pas entièrement remédier à cette faille.

### Points Clés :

*   **Attaques automatisées:** Exploitation rapide et à grande échelle.
*   **Création de comptes non autorisés:** Ajout d'utilisateurs avec accès VPN.
*   **Vol de configurations:** Extraction des paramètres du pare-feu.
*   **Exploitation potentielle de contournement de patchs:** Les correctifs précédents pourraient ne pas être suffisants.

### Vulnérabilités :

*   **CVE-2025-59718:** Vulnérabilité critique de contournement d'authentification SSO affectant FortiGate via FortiCloud SSO.
*   Une vulnérabilité inconnue dans la fonction SSO est exploitée dans la campagne actuelle.

### Recommandations :

*   **Désactiver le SSO FortiCloud (temporairement):** Jusqu'à ce que Fortinet fournisse un correctif définitif, il est recommandé de désactiver la fonctionnalité "Allow administrative login using FortiCloud SSO" dans les paramètres du système (System -> Settings) ou via l'interface en ligne de commande :
    ```
    config system global
    set admin-forticloud-sso-login disable
    end
    ```
*   **Surveillance active:** Tenir compte des indicateurs de compromission partagés par les chercheurs en cybersécurité, tels que la création d'utilisateurs admin via SSO depuis `cloud-init@mail.io` sur des adresses IP spécifiques.
*   **Mise à jour vers les versions futures:** Fortinet prévoit de publier des mises à jour (FortiOS 7.4.11, 7.6.6, et 8.0.0) pour adresser complètement cette faille. Il est crucial de les appliquer dès leur disponibilité.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-breach-fortinet-fortigate-devices-steal-firewall-configs/){:target="_blank"}
