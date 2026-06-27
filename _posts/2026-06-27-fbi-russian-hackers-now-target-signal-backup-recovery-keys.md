---
title: 'FBI: Russian hackers now target Signal backup recovery keys'
date: 2026-06-27
permalink: /posts/2026/06/27/fbi-russian-hackers-now-target-signal-backup-recovery-keys/
tags:
- veille-cyber
- bleepingcomp
---
### Espionnage : Campagne de phishing russe ciblant les clés de sauvegarde Signal

Le FBI et la CISA alertent sur une évolution des tactiques de phishing menées par les services de renseignement russes (groupes UNC5792 et UNC4221). Ces acteurs ciblent des profils à haute valeur ajoutée (responsables gouvernementaux, militaires, journalistes) pour compromettre l'historique de leurs messages Signal.

**Points clés :**
*   **Tactique :** Les attaquants se font passer pour le support technique de Signal via des messages frauduleux affirmant qu'une vérification en deux étapes est obligatoire.
*   **Objectif :** Inciter les victimes à générer une clé de récupération de sauvegarde, puis à leur transmettre cette clé sous prétexte de résoudre un faux problème de synchronisation.
*   **Conséquences :** Une fois la clé en leur possession, les attaquants peuvent restaurer et déchiffrer les sauvegardes des conversations (privées et de groupe) sur leurs propres appareils.
*   **Persistance :** Changer de numéro de téléphone ou réinitialiser le compte ne suffit pas à invalider une clé déjà volée ; les attaquants conservent l'accès aux données déjà téléchargées.

**Vulnérabilités :**
*   Aucune vulnérabilité technique (CVE) du logiciel Signal n'est exploitée. Il s'agit d'une attaque par ingénierie sociale visant à détourner les fonctionnalités légitimes de sauvegarde chiffrée de l'application.

**Recommandations :**
*   **Ne jamais partager sa clé de sauvegarde :** Le personnel officiel de Signal ne demande jamais de codes de vérification, de clés de récupération ou d'informations d'identification via l'application.
*   **Gestion des clés :** En cas de compromission suspectée, générez immédiatement une nouvelle clé de récupération dans les paramètres de Signal. Cela invalidera l'ancienne clé pour toute nouvelle sauvegarde, bien que les données déjà téléchargées par l'attaquant restent exposées.
*   **Vigilance sur les communications :** Toute demande de "mise à jour de sécurité" ou de "synchronisation" reçue par messagerie doit être considérée comme suspecte.
*   **Signalement :** Signaler toute tentative d'intrusion aux autorités compétentes (IC3 pour le FBI ou organismes de cybersécurité locaux).

---
[Source](https://www.bleepingcomputer.com/news/security/fbi-russian-hackers-now-target-signal-backup-recovery-keys/){:target="_blank"}
