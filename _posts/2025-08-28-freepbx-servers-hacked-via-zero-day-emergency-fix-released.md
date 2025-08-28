---
title: 'FreePBX servers hacked via zero-day, emergency fix released'
date: 2025-08-28
permalink: /posts/2025/08/28/freepbx-servers-hacked-via-zero-day-emergency-fix-released/
tags:
- veille-cyber
- bleepingcomp
---
**Exploitation d'une faille zero-day sur FreePBX : un correctif d'urgence disponible**

Des serveurs FreePBX exposés sur Internet ont été compromis par une vulnérabilité zero-day exploitée activement depuis le 21 août. Cette faille affecte les systèmes où le panneau de contrôle administrateur (ACP) est accessible publiquement. Des entreprises ont signalé des intrusions massives, affectant des milliers d'extensions et de trunks SIP. Les attaquants peuvent exécuter des commandes sur les systèmes affectés.

**Points Clés :**

*   **Nature de la menace :** Exploitation d'une vulnérabilité zero-day sur le panneau de contrôle administrateur de FreePBX.
*   **Impact :** Compromission de serveurs, exécution de commandes par les attaquants, potentielle utilisation abusive des ressources de téléphonie.
*   **Versions affectées :** FreePBX v16 et v17, notamment si le module "endpoint" est installé et si l'interface administrateur est exposée à Internet.
*   **Indicateurs de compromission (IOC) :** Fichier `/etc/freepbx.conf` manquant ou modifié, présence du script `/var/www/html/.clean.sh`, entrées suspectes dans les logs Apache concernant `modular.php`, appels inhabituels vers l'extension `9998` dans les logs Asterisk, entrées non autorisées dans la table `ampusers` de la base de données.

**Vulnérabilités :**

*   Aucun identifiant CVE spécifique n'est mentionné dans l'article pour cette faille zero-day.

**Recommandations :**

*   **Accès restreint :** Limiter l'accès au panneau d'administration FreePBX via le module Firewall, en autorisant uniquement les hôtes de confiance.
*   **Application du correctif :** Les utilisateurs des versions v16 et v17 peuvent tester le module "EDGE" en exécutant :
    *   `fwconsole ma downloadinstall endpoint --edge` (pour FreePBX v16/v17)
    *   `fwconsole ma downloadinstall endpoint --tag 16.0.88.19` (pour PBXAct v16)
    *   `fwconsole ma downloadinstall endpoint --tag 17.0.2.31` (pour PBXAct v17)
*   **Mesures en cas d'impossibilité d'installer le correctif :** Bloquer l'accès au panneau de contrôle administrateur jusqu'à la sortie d'une mise à jour de sécurité complète.
*   **En cas de compromission avérée :**
    *   Restaurer à partir de sauvegardes antérieures au 21 août.
    *   Déployer les modules corrigés sur des systèmes propres.
    *   Changer tous les identifiants système et SIP.
    *   Examiner les journaux d'appels et les factures téléphoniques pour détecter toute utilisation abusive, notamment des communications internationales non autorisées.
*   **Investigation :** Les administrateurs sont invités à investiguer leurs installations et à sécuriser leurs systèmes même s'ils n'ont pas encore observé d'impact.

---
[Source](https://www.bleepingcomputer.com/news/security/freepbx-servers-hacked-via-zero-day-emergency-fix-released/){:target="_blank"}
