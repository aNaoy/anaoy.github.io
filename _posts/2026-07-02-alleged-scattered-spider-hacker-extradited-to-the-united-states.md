---
title: 'Alleged Scattered Spider hacker extradited to the United States'
date: 2026-07-02
permalink: /posts/2026/07/02/alleged-scattered-spider-hacker-extradited-to-the-united-states/
tags:
- veille-cyber
- bleepingcomp
---
### Extradition d'un membre clé du collectif Scattered Spider

Peter Stokes, un ressortissant américano-estonien de 19 ans, a été extradé vers les États-Unis après son arrestation en Finlande. Il est accusé d'être un membre actif du groupe de cybercriminels **Scattered Spider** (également connu sous les noms de UNC3944, 0ktapus ou Octo Tempest), responsable de plus de 100 intrusions réseau et de dommages dépassant 100 millions de dollars.

**Points clés :**
*   **Mode opératoire :** Le groupe privilégie l'ingénierie sociale (usurpation d'identité auprès des services d'assistance informatique), le phishing par SMS et les attaques par fatigue MFA (bombardement de notifications d'authentification multifacteur).
*   **Outils :** Utilisation fréquente d'émulateurs Android (comme Genymobile) pour orchestrer les attaques MFA et déploiement du ransomware DragonForce.
*   **Cibles :** Organisations de haut profil (Caesars, MGM Resorts, Twilio, Reddit, etc.) avec pour objectif l'extorsion de données sensibles suivies de demandes de rançon multimillionnaires.

**Vulnérabilités exploitées :**
*   **Facteur humain :** Manipulation du personnel des centres de support informatique pour obtenir des réinitialisations de mots de passe ou des accès administrateur (aucune CVE spécifique, car il s'agit d'attaques d'ingénierie sociale).
*   **Failles MFA :** Exploitation de la lassitude des utilisateurs face aux demandes répétées d'authentification.

**Recommandations de sécurité :**
*   **Renforcement de l'authentification :** Privilégier des méthodes d'authentification MFA résistantes au phishing (ex: clés de sécurité matérielles FIDO2/WebAuthn) plutôt que les SMS ou les notifications push classiques.
*   **Procédures de support :** Établir des protocoles stricts de vérification d'identité pour toute demande de réinitialisation de compte ou de modification d'accès adressée au helpdesk.
*   **Sensibilisation :** Former les employés aux techniques d'ingénierie sociale et aux risques liés au "MFA fatigue".

---
[Source](https://www.bleepingcomputer.com/news/security/alleged-scattered-spider-hacker-extradited-to-the-united-states/){:target="_blank"}
