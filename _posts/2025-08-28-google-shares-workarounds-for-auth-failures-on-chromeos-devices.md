---
title: 'Google shares workarounds for auth failures on ChromeOS devices'
date: 2025-08-28
permalink: /posts/2025/08/28/google-shares-workarounds-for-auth-failures-on-chromeos-devices/
tags:
- veille-cyber
- bleepingcomp
---
**Problèmes d'authentification sur ChromeOS : Solutions temporaires et impacts**

Des dysfonctionnements d'authentification affectent certains appareils fonctionnant sous ChromeOS, version 16328.55.0, avec le navigateur Chrome version 139.0.7258.137. Ces problèmes empêchent les utilisateurs de se connecter à des plateformes éducatives clés telles que Clever et ClassLink, qui gèrent l'accès des élèves aux ressources numériques. L'authentification à deux facteurs (2SV) peut également être impactée, limitant l'accès à certains services Google.

Ces problèmes impactent de manière significative des millions d'élèves et d'enseignants qui dépendent de ces outils pour leur accès à l'éducation numérique.

**Points clés :**

*   Des problèmes d'authentification bloquent l'accès aux comptes Clever et ClassLink sur certains appareils ChromeOS.
*   Les versions logicielles concernées sont ChromeOS 16328.55.0 et Chrome 139.0.7258.137.
*   L'authentification à deux facteurs peut également être affectée.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. Le problème semble résider dans un défaut de la procédure d'authentification elle-même, potentiellement lié à une mise à jour logicielle.

**Recommandations :**

Pour contourner le problème en attendant un correctif officiel :

1.  **Rétrogradation de la version de ChromeOS :** Les administrateurs peuvent ramener les appareils à la version M138 de ChromeOS. Cela implique de se connecter à la console d'administration Google, de naviguer dans les paramètres des appareils Chrome, de sélectionner l'unité organisationnelle concernée, de configurer les paramètres de mise à jour des appareils pour permettre la rétrogradation vers une version cible (M138), puis de sauvegarder les modifications.
2.  **Modification du paramètre `LoginAuthenticationBehavior` :** Les administrateurs peuvent modifier ce paramètre pour utiliser "l'authentification via le flux GAIA par défaut", ce qui contourne la voie d'authentification problématique.

Google a indiqué que des tests automatisés sont en cours pour un correctif définitif, mais aucune date de publication n'a été communiquée. Une mise à jour des informations est prévue pour le jeudi 28 août 2025, 17h30 (heure du Pacifique).

---
[Source](https://www.bleepingcomputer.com/news/google/google-shares-chromeos-workarounds-for-clever-classlink-auth-failures/){:target="_blank"}
