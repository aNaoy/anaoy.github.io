---
title: 'October 2026 Microsoft Patch Tuesday, (Tue, Oct 13th)'
date: 2026-10-14
permalink: /posts/2026/10/14/october-2026-microsoft-patch-tuesday-tue-oct-13th/
tags:
- veille-cyber
- sans-isc
---
### Rapport de sécurité : Microsoft Patch Tuesday (Octobre 2026)

Le Patch Tuesday d'octobre 2026 de Microsoft corrige **1 417 vulnérabilités**, dont 76 sont classées critiques. Sept de ces vulnérabilités critiques ne nécessitent aucune intervention de l'utilisateur.

#### Points clés
*   Une vulnérabilité est actuellement activement exploitée ("exploited in the wild").
*   Une vulnérabilité a été rendue publique avant la publication des correctifs.
*   Un nombre important de vulnérabilités touchent la suite **Microsoft Office**, nécessitant une attention particulière.
*   Plusieurs vulnérabilités d'exécution de code à distance (RCE) ont été identifiées dans les serveurs DHCP Windows.

#### Vulnérabilités majeures
*   **CVE-2026-96951** : Contournement de la fonctionnalité de sécurité Windows Shell ("Mark of the Web"). Déjà activement exploitée, cette faille permet une exécution de code via des messages malveillants (e-mail ou messagerie instantanée), sous réserve que la victime ouvre le fichier.
*   **CVE-2026-108398** : Contournement de la fonctionnalité de sécurité .NET framework. Permet le contournement du contrôle des applications. Bien que les détails aient été rendus publics, aucune exploitation active n'a été détectée par Microsoft à ce jour.
*   **CVE-2026-70571** : RCE dans Microsoft Exchange Server. La complexité de l'attaque est élevée, nécessitant l'envoi d'un e-mail spécifique déclenchant la faille durant la conversion de contenu.

#### Recommandations
1.  **Priorisation des correctifs** : Appliquer en priorité les mises à jour concernant la suite Microsoft Office en raison du volume élevé de vulnérabilités découvertes.
2.  **Gestion des serveurs** : Déployer rapidement les correctifs pour les serveurs Windows DHCP, particulièrement les 5 vulnérabilités critiques identifiées.
3.  **Vigilance accrue** : La vulnérabilité **CVE-2026-96951** étant déjà exploitée, les équipes de sécurité doivent surveiller les vecteurs d'entrée (e-mails et messageries) utilisés pour diffuser les fichiers malveillants.
4.  **Mise à jour globale** : Étant donné le nombre massif de CVE traitées ce mois-ci, une campagne de mise à jour complète de l'infrastructure est recommandée dès que possible pour mitiger les risques d'élévation de privilèges et de RCE.

---
[Source](https://isc.sans.edu/diary/rss/33422){:target="_blank"}
