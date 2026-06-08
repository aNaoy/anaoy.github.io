---
title: 'Critical UniFi OS bug lets hackers gain root without authentication'
date: 2026-06-08
permalink: /posts/2026/06/08/critical-unifi-os-bug-lets-hackers-gain-root-without-authentication/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique : Exécution de code à distance sur UniFi OS

Des chercheurs ont démontré qu'en enchaînant trois vulnérabilités corrigées en mai dernier, un attaquant peut obtenir un accès root total sur les serveurs UniFi OS (versions 5.0.6 et antérieures) sans aucune authentification ni interaction utilisateur. Cette faille permet une prise de contrôle administrative complète sur l'infrastructure réseau gérée par l'appareil.

**Points clés :**
*   **Chaînage d'attaques :** Le contournement de l'authentification est rendu possible par une discordance entre la validation des URI par UniFi OS et le routage par Nginx, permettant d'accéder à des endpoints protégés.
*   **Escalade de privilèges :** Une fois l'accès initial obtenu via injection de commande, l'attaquant exploite les privilèges `sudo` sans mot de passe d'un compte de service pour obtenir les droits root.
*   **Difficulté de détection :** L'absence d'authentification signifie qu'aucune trace de tentative de connexion échouée n'est générée, rendant la détection d'une compromission antérieure particulièrement complexe.

**Vulnérabilités associées :**
*   **CVE-2026-34908 :** Contrôle d'accès inapproprié permettant de manipuler les systèmes vulnérables.
*   **CVE-2026-34909 :** Traversée de répertoire (*path traversal*) exposant des fichiers du système.
*   **CVE-2026-34910 :** Injection de commande permettant l'exécution de code arbitraire.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer la mise à jour vers **UniFi OS Server 5.0.8 ou version ultérieure**.
*   **Audit de sécurité :** Vérifier l'intégrité du système avant la mise à jour, car celle-ci ne supprime pas les backdoors ou mécanismes de persistance déjà installés.
*   **Détection :**
    *   Utiliser le script de détection fourni par [Bishop Fox](https://github.com/BishopFox/CVE-2026-34908-check) pour tester l'exposition des instances.
    *   Surveiller les logs pour des requêtes suspectes vers `/api/auth/validate-sso/` et `ucs/update/latest_package`.
    *   Surveiller les processus enfants suspects sous `ucs-update` ainsi que les commandes `sudo` inhabituelles.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-unifi-os-bug-lets-hackers-gain-root-without-authentication/){:target="_blank"}
