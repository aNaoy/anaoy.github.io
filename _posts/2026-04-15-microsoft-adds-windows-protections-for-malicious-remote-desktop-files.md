---
title: 'Microsoft adds Windows protections for malicious Remote Desktop files'
date: 2026-04-15
permalink: /posts/2026/04/15/microsoft-adds-windows-protections-for-malicious-remote-desktop-files/
tags:
- veille-cyber
- bleepingcomp
---
### Renforcement de la sécurité Windows face aux fichiers RDP malveillants

Microsoft a déployé de nouvelles mesures de protection dans les mises à jour cumulatives d'avril 2026 (KB5082200, KB5083769 et KB5082052) pour contrer les campagnes de phishing exploitant les fichiers de connexion Bureau à distance (.rdp). Ces fichiers sont détournés par des acteurs malveillants (notamment le groupe APT29) pour exfiltrer des données, voler des identifiants ou intercepter le contenu du presse-papiers et des périphériques locaux.

**Points clés :**
*   **Alerte pédagogique :** Lors de la première ouverture d'un fichier RDP, une notification explique les risques associés.
*   **Dialogue de sécurité renforcé :** Avant toute connexion, Windows affiche désormais une fenêtre de confirmation détaillant l'adresse distante et les ressources partagées.
*   **Désactivation par défaut :** Toutes les redirections de ressources locales (lecteurs, presse-papiers, appareils) sont désormais désactivées par défaut dans ces boîtes de dialogue.
*   **Vérification de signature :** Le système signale clairement si l'éditeur est inconnu ou non vérifié.

**Vulnérabilités :**
*   Le vecteur d'attaque principal repose sur l'abus de la fonctionnalité de redirection automatique des ressources locales dans les fichiers RDP. Aucun identifiant CVE n'est associé à cette mise à jour, car il s'agit d'une amélioration de conception sécuritaire ("Security by Design") visant à limiter l'exploitation abusive d'une fonctionnalité légitime.

**Recommandations :**
*   **Maintenir les protections :** Il est fortement déconseillé de désactiver ces alertes.
*   **Gestion centralisée :** Bien qu'il soit techniquement possible pour les administrateurs de désactiver ces nouvelles protections via la clé de registre `HKLM\Software\Policies\Microsoft\Windows NT\Terminal Services\Client` (valeur `RedirectionWarningDialogVersion` réglée sur `1`), Microsoft préconise de les laisser actives pour bloquer efficacement les tentatives de phishing.
*   **Vigilance utilisateur :** S'assurer que les utilisateurs finaux comprennent la nécessité de vérifier l'origine et la signature numérique des fichiers RDP avant toute connexion.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-adds-windows-protections-for-malicious-remote-desktop-files/){:target="_blank"}
