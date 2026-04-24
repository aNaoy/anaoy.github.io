---
title: 'New ‘Pack2TheRoot’ flaw gives hackers root Linux access'
date: 2026-04-24
permalink: /posts/2026/04/24/new-pack2theroot-flaw-gives-hackers-root-linux-access/
tags:
- veille-cyber
- bleepingcomp
---
### Pack2TheRoot : Une vulnérabilité critique affectant PackageKit

La faille **Pack2TheRoot** permet à un utilisateur local non privilégié d'installer ou de supprimer des paquets système sur Linux, menant à une élévation de privilèges vers le compte "root". Présente depuis 2014, cette vulnérabilité touche une large gamme de distributions Linux utilisant le service PackageKit.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-41651 (Score de sévérité : 8.8/10).
*   **Cause :** Un défaut dans le mécanisme de gestion des requêtes du démon PackageKit, permettant à certaines commandes (ex: `pkcon install`) de contourner l'authentification requise.
*   **Portée :** Affecte les versions de PackageKit de 1.0.2 à 1.3.4. Toutes les distributions Linux intégrant ce service par défaut sont potentiellement exposées (notamment Ubuntu, Debian, RockyLinux et Fedora).
*   **Indicateur de compromission :** L'exploitation provoque une erreur d'assertion et le plantage du démon PackageKit, un événement traçable dans les journaux système.

**Recommandations :**
*   **Mise à jour :** Installer immédiatement la version **1.3.5** de PackageKit, qui corrige cette faille.
*   **Vérification :** Utiliser les commandes `dpkg -l | grep -i packagekit` (Debian/Ubuntu) ou `rpm -qa | grep -i packagekit` (Fedora/Rocky) pour identifier la version installée.
*   **Surveillance :** Vérifier l'état du démon via `systemctl status packagekit` et inspecter les journaux système pour détecter d'éventuels plantages suspects du service.

---
[Source](https://www.bleepingcomputer.com/news/security/new-pack2theroot-flaw-gives-hackers-root-linux-access/){:target="_blank"}
