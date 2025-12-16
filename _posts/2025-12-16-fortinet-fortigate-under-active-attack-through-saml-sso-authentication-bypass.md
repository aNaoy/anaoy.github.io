---
title: 'Fortinet FortiGate Under Active Attack Through SAML SSO Authentication Bypass'
date: 2025-12-16
permalink: /posts/2025/12/16/fortinet-fortigate-under-active-attack-through-saml-sso-authentication-bypass/
tags:
- veille-cyber
- hackernews
---
**Exploitation Active de Vulnérabilités FortiGate : Contournement de l'Authentification SAML SSO**

Des acteurs malveillants exploitent activement deux vulnérabilités critiques sur les appareils FortiGate de Fortinet, moins d'une semaine après leur divulgation publique. Ces failles permettent un contournement non authentifié de l'authentification par connexion unique (SSO) SAML, à condition que la fonctionnalité FortiCloud SSO soit activée. L'activation de FortiCloud SSO est automatique lors de l'enregistrement FortiCare, sauf si elle est explicitement désactivée.

Les attaques observées utilisent des adresses IP issues de fournisseurs d'hébergement spécifiques pour effectuer des connexions SSO malveillantes sur le compte "admin", suivies de l'exportation de configurations d'appareils.

**Points Clés :**

*   Exploitation active de vulnérabilités FortiGate depuis le 12 décembre 2025.
*   Utilisation de messages SAML fabriqués pour contourner l'authentification.
*   Les attaquants exportent les configurations des appareils compromis.

**Vulnérabilités :**

*   CVE-2025-59718 (CVSS 9.8)
*   CVE-2025-59719 (CVSS 9.8)

Ces deux vulnérabilités permettent un contournement de l'authentification SSO, en particulier lorsque la fonctionnalité FortiCloud SSO est activée.

**Recommandations :**

*   Appliquer les correctifs de sécurité publiés par Fortinet pour FortiOS, FortiWeb, FortiProxy et FortiSwitchManager dans les plus brefs délais.
*   Désactiver la fonctionnalité FortiCloud SSO jusqu'à la mise à jour des systèmes affectés.
*   Restreindre l'accès aux interfaces de gestion des pare-feu et des VPN aux seuls utilisateurs internes de confiance.
*   En cas d'indicateurs de compromission, considérer l'appareil comme compromis et réinitialiser les identifiants (hashés) des pare-feu qui auraient été exportés.

---
[Source](https://thehackernews.com/2025/12/fortinet-fortigate-under-active-attack.html){:target="_blank"}
