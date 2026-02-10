---
title: 'Hackers breach SmarterTools network using flaw in its own software'
date: 2026-02-10
permalink: /posts/2026/02/10/hackers-breach-smartertools-network-using-flaw-in-its-own-software/
tags:
- veille-cyber
- bleepingcomp
---
### Intrusion chez SmarterTools via une faille de sécurité

Le réseau de SmarterTools a été compromis par le groupe de ransomware Warlock, qui a exploité une vulnérabilité dans le logiciel SmarterMail. L'intrusion a eu lieu le 29 janvier via une machine virtuelle SmarterMail non mise à jour, exploitant ainsi une faille permettant le contournement de l'authentification et la réinitialisation des mots de passe administrateur. Bien que les données clients n'aient pas été directement touchées, douze serveurs Windows et un centre de données secondaire ont été affectés. Les attaquants ont ensuite utilisé des outils comme Velociraptor pour se déplacer latéralement et établir la persistance, avant d'être finalement bloqués dans leur tentative de chiffrement par des solutions de sécurité. Cette activité est associée au groupe Storm-2603, potentiellement lié à un acteur d'État chinois. Une autre faille, CVE-2026-24423, a également été identifiée comme étant exploitée.

**Points Clés :**

*   **Acteur de la menace :** Groupe Warlock, potentiellement lié à Storm-2603 (acteurs étatiques chinois).
*   **Vecteur d'attaque initial :** Machine virtuelle SmarterMail non mise à jour.
*   **Techniques post-exploitation :** Mouvement latéral via Active Directory, utilisation d'outils comme Velociraptor, SimpleHelp, WinRAR, et de mécanismes de persistance (entrées de démarrage, tâches planifiées).
*   **Impact :** Compromission de serveurs Windows et d'un centre de données secondaire.
*   **Protection :** Les solutions de sécurité ont empêché le chiffrement final des données.

**Vulnérabilités :**

*   **CVE-2026-23760 :** Contournement de l'authentification dans SmarterMail (avant Build 9518), permettant la réinitialisation des mots de passe administrateur et l'obtention de privilèges complets.
*   **CVE-2026-24423 :** Faille dans SmarterMail permettant l'exécution de code à distance (RCE).

**Recommandations :**

*   **Mettre à jour SmarterMail vers la version Build 9511 ou une version ultérieure.**
*   Assurer la mise à jour régulière de toutes les instances logicielles, y compris celles qui pourraient être moins visiblement déployées.
*   Surveiller les activités suspectes, notamment l'utilisation d'outils de forensics pour des activités malveillantes.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-breach-smartertools-network-using-flaw-in-its-own-software/){:target="_blank"}
