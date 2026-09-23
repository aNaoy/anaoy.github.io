---
title: 'MikroTrick Chain Let Attackers Take Over MikroTik Routers Without a Password or SSH Key'
date: 2026-09-23
permalink: /posts/2026/09/23/mikrotrick-chain-let-attackers-take-over-mikrotik-routers-without-a-password-or-ssh-key/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique « MikroTrick » sur MikroTik RouterOS

Une chaîne d'exploitation baptisée **MikroTrick** permet aux attaquants de prendre le contrôle administratif complet de routeurs MikroTik exposés à Internet, sans nécessiter de mot de passe ni de clé SSH.

#### Points clés
*   L'attaque combine deux vulnérabilités pour contourner l'authentification et injecter des privilèges administrateur.
*   L'exploitation a été observée dès le 2 septembre, juste avant la publication des correctifs.
*   Les attaquants ont utilisé cette faille pour créer des comptes utilisateurs malveillants (ex: `ops`) et exfiltrer des données de configuration.

#### Vulnérabilités exploitées
*   **CVE-2026-67279** : Défaut dans la machine d'état SSH permettant de passer à la phase de commande sans authentification réussie via une renégociation de clé.
*   **CVE-2026-86060** : Injection d'arguments dans le programme de connexion (`/nova/bin/login`), permettant de détourner le processus d'authentification en envoyant `-2` comme nom d'utilisateur.

#### Recommandations
1.  **Mise à jour immédiate** : Appliquer les correctifs RouterOS (versions 6.49.21, 7.23.4, 7.24.2 ou supérieures).
2.  **Audit post-compromission** :
    *   Vérifier la présence de comptes inconnus, de scripts suspects, de tunnels ou de tâches planifiées.
    *   Inspecter les logs pour l'utilisateur `-2`.
    *   Vérifier le statut `Flagged` via `/system/device-mode/print`.
3.  **Récupération** : En cas de compromission avérée, ne pas restaurer de sauvegarde. Isoler l'appareil, effectuer une réinitialisation d'usine, reconstruire la configuration manuellement et renouveler tous les identifiants/clés.
4.  **Durcissement** : Restreindre l'accès SSH en limitant l'exposition aux réseaux publics via les règles de pare-feu.

---
[Source](https://thehackernews.com/2026/09/mikrotrick-chain-let-attackers-take.html){:target="_blank"}
