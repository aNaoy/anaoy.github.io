---
title: 'Hackers breach TrueConf to trojanize client installers with backdoors'
date: 2026-08-08
permalink: /posts/2026/08/08/hackers-breach-trueconf-to-trojanize-client-installers-with-backdoors/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission des serveurs TrueConf par le groupe Head Mare

Le groupe de hacktivistes "Head Mare" mène actuellement des cyberattaques contre les serveurs de visioconférence TrueConf, largement utilisés dans les secteurs gouvernementaux et industriels en Russie. L'objectif est d'injecter des portes dérobées dans les installateurs clients légitimes afin de compromettre les terminaux des utilisateurs.

**Points clés :**
*   **Méthode d'attaque :** Les attaquants exploitent des serveurs non mis à jour pour obtenir des privilèges administrateur (NT AUTHORITY\SYSTEM), puis remplacent les installateurs clients par des versions malveillantes.
*   **Propagation :** Lorsqu'un utilisateur se connecte à un serveur compromis (ou à celui d'un partenaire), il reçoit une mise à jour infectée non signée numériquement.
*   **Logiciels malveillants déployés :** 
    *   **PhantomCore :** Porté par l'installateur piégé.
    *   **PhantomGraph :** Utilise OneDrive comme canal de commande et de contrôle (C2) pour exfiltrer des identifiants via le dump du processus LSASS et établir des tunnels SSH inversés.
*   **Cibles :** Organisations russes dans les secteurs de l'énergie, du transport, de l'IT et de l'électronique.

**Vulnérabilités :**
*   **KLCERT-26-057 :** Exécution de script dans l'environnement isolé de TrueConf.
*   **KLCERT-26-058 :** Évasion du bac à sable (sandbox) permettant l'exécution de commandes sur le système d'exploitation hôte.
*   **CVE-2026-3502 :** Faille d'exécution arbitraire de fichier (déjà identifiée précédemment dans "Operation True Chaos").

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs fournis par l'éditeur le 18 juin 2026. Les versions sécurisées sont :
    *   **5.3.9** (pour la branche 5.3.x)
    *   **5.4.9** (pour la branche 5.4.x)
    *   **5.5.5** (pour la branche 5.5.x)
*   **Vigilance des utilisateurs :** Se méfier des installateurs ou mises à jour de logiciels qui ne sont pas signés numériquement ou qui proviennent de sources non vérifiées.
*   **Surveillance réseau :** Surveiller toute activité suspecte sur le port TCP 4307 et restreindre son accès aux sources légitimes uniquement.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-breach-trueconf-to-trojanize-client-installers-with-backdoors/){:target="_blank"}
