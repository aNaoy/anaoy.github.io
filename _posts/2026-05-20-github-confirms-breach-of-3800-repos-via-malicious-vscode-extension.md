---
title: 'GitHub confirms breach of 3,800 repos via malicious VSCode extension'
date: 2026-05-20
permalink: /posts/2026/05/20/github-confirms-breach-of-3800-repos-via-malicious-vscode-extension/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de GitHub via une extension VS Code piégée

GitHub a confirmé l'exfiltration d'environ 3 800 de ses dépôts internes suite à l'installation d'une extension VS Code malveillante sur l'appareil d'un employé. Le groupe de cybercriminels "TeamPCP", déjà identifié dans de nombreuses attaques contre la chaîne d'approvisionnement logicielle, revendique cette intrusion et tente de vendre les données dérobées pour au moins 50 000 dollars.

**Points clés :**
*   **Vecteur d'attaque :** Une extension VS Code "trojanisée" installée depuis le Marketplace officiel.
*   **Impact :** Environ 3 800 dépôts internes de GitHub ont été compromis.
*   **État actuel :** GitHub a retiré l'extension incriminée, isolé le poste de travail infecté et lancé une procédure de réponse à incident. Aucune preuve d'impact sur les données des clients externes n'a été constatée à ce stade.
*   **Historique :** Le Marketplace VS Code est régulièrement ciblé par des campagnes de logiciels malveillants (infostealers, cryptominers, ransomware) se faisant passer pour des outils de développement légitimes.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cette attaque, celle-ci reposant sur l'exécution d'un code malveillant via le système de plugins de VS Code, exploitant la confiance des utilisateurs envers le Marketplace officiel.

**Recommandations :**
*   **Vigilance sur les extensions :** Limiter l'installation d'extensions VS Code aux outils vérifiés et nécessaires. Examiner systématiquement les permissions demandées avant l'installation.
*   **Gestion des accès :** Appliquer le principe du moindre privilège sur les postes de travail des développeurs pour limiter les conséquences d'une éventuelle compromission.
*   **Surveillance :** Renforcer la surveillance du trafic réseau sortant depuis les environnements de développement pour détecter rapidement des exfiltrations de données vers des serveurs inconnus.
*   **Politiques de sécurité :** Mettre en place des politiques d'entreprise strictes interdisant l'utilisation d'outils tiers non validés sur les postes accédant à du code source sensible.

---
[Source](https://www.bleepingcomputer.com/news/security/github-confirms-breach-of-3-800-repos-via-malicious-vscode-extension/){:target="_blank"}
