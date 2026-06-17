---
title: 'Junior Hacker Used Tailscale and OpenSSH to Keep Access After His C2 Went Offline'
date: 2026-06-17
permalink: /posts/2026/06/17/junior-hacker-used-tailscale-and-openssh-to-keep-access-after-his-c2-went-offline/
tags:
- veille-cyber
- hackernews
---
### Persistance post-C2 : L'utilisation détournée d'outils légitimes

Une enquête sur l'attaquant "Poisson" révèle comment un acteur de menace junior a maintenu l'accès à un réseau d'entreprise française même après la déconnexion de son serveur de commande et de contrôle (C2) Havoc. En installant des outils de gestion légitimes avant la chute de son C2, l'attaquant a assuré sa persistance, démontrant que la neutralisation d'un serveur C2 est insuffisante si les portes dérobées secondaires ne sont pas identifiées.

**Points clés :**
*   **Stratégie de persistance :** Utilisation d'OpenSSH et de Tailscale pour créer un tunnel inverse, permettant de contourner le C2 et d'accéder à la machine via un réseau privé chiffré.
*   **Techniques employées :** Injection de code en mémoire (via VBScript et PowerShell), utilisation de RustDesk comme canal de secours et déploiement d'un keylogger Python pour le vol d'identifiants bancaires et emails.
*   **Failles opérationnelles :** Malgré des erreurs de débutant (fuites de répertoires, usage de services gratuits), l'attaquant a compromis quatre machines sur une période de 33 jours.
*   **Vulnérabilités exploitées :** Aucune vulnérabilité logicielle spécifique (CVE) n'est mentionnée ; l'attaque repose sur l'usage détourné d'outils d'administration légitimes et sur l'élévation de privilèges par interaction humaine via l'invite de consentement Windows (`Start-Process -Verb RunAs`).

**Recommandations :**
*   **Surveillance comportementale :** Détecter l'installation d'OpenSSH sur des stations de travail Windows et la présence inattendue de `tailscale.exe`.
*   **Analyse des connexions :** Surveiller les tunnels SSH inverses (`ssh -R`) et les connexions sortantes vers des services dynamiques (type DuckDNS).
*   **Contrôle des privilèges :** Auditer les tâches planifiées s'exécutant avec les privilèges les plus élevés et les scripts `wscript.exe` lancés depuis des dossiers utilisateur.
*   **Gestion des incidents :** Lors de la découverte d'un C2, ne jamais considérer l'infrastructure principale comme l'unique point d'entrée. Rechercher systématiquement les mécanismes de persistance persistants (VPN, outils d'accès à distance, tâches planifiées).

---
[Source](https://thehackernews.com/2026/06/junior-hacker-used-tailscale-and.html){:target="_blank"}
