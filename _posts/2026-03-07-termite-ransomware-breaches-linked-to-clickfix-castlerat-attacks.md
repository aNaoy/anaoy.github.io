---
title: 'Termite ransomware breaches linked to ClickFix CastleRAT attacks'
date: 2026-03-07
permalink: /posts/2026/03/07/termite-ransomware-breaches-linked-to-clickfix-castlerat-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Infiltration par la technique ClickFix : Le mode opératoire de Velvet Tempest

Le groupe cybercriminel Velvet Tempest (également connu sous le nom de DEV-0504) exploite la technique d'ingénierie sociale « ClickFix » pour infiltrer des réseaux d'entreprise, déployant notamment le malware DonutLoader et le cheval de Troie d'accès à distance (RAT) CastleRAT. Bien que ce groupe soit historiquement lié à de nombreuses souches de ransomwares, dont le récent ransomware Termite, cette campagne spécifique s'est concentrée sur l'accès initial, la reconnaissance Active Directory et l'exfiltration de données sans chiffrement final.

**Points clés :**
*   **Vecteur d'attaque :** Campagne de malvertising utilisant une interface trompeuse (ClickFix) simulant une vérification CAPTCHA.
*   **Exécution :** La victime est manipulée pour copier-coller une commande malveillante dans l'outil « Exécuter » de Windows, déclenchant des chaînes de commandes `cmd.exe`.
*   **Living-off-the-land :** Utilisation détournée d'outils légitimes Windows (`finger.exe`, `csc.exe`, PowerShell) pour télécharger des payloads, compiler des composants .NET et assurer la persistance.
*   **Objectifs :** Profilage environnemental, découverte d'hôtes et vol d'identifiants stockés dans les navigateurs (Chrome).

**Vulnérabilités :**
*   L'attaque repose sur l'ingénierie sociale et l'abus de fonctionnalités natives de Windows (Living-off-the-land). Aucun exploit de vulnérabilité spécifique (CVE) n'est cité pour l'accès initial, le succès reposant sur l'exécution volontaire de commandes par l'utilisateur.

**Recommandations :**
*   **Sensibilisation :** Former les employés aux dangers du copier-coller de commandes provenant de sites Web, même si celles-ci semblent provenir de processus de vérification légitimes (CAPTCHA).
*   **Restriction des privilèges :** Restreindre l'exécution de scripts PowerShell et l'utilisation d'outils système (comme `csc.exe` ou `finger.exe`) aux utilisateurs et comptes non autorisés.
*   **Surveillance EDR :** Configurer des alertes sur les comportements suspects de type « Living-off-the-land », notamment l'utilisation de `cmd.exe` lancée depuis des dialogues de commande ou la compilation inattendue de code .NET en temps réel.
*   **Gestion des identifiants :** Éviter de stocker des mots de passe sensibles dans les navigateurs ; privilégier l'usage de gestionnaires de mots de passe sécurisés ou de solutions de gestion des accès (PAM).

---
[Source](https://www.bleepingcomputer.com/news/security/termite-ransomware-breaches-linked-to-clickfix-castlerat-attacks/){:target="_blank"}
