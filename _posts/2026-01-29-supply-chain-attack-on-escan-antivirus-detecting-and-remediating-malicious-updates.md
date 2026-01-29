---
title: 'Supply chain attack on eScan antivirus: detecting and remediating malicious updates'
date: 2026-01-29
permalink: /posts/2026/01/29/supply-chain-attack-on-escan-antivirus-detecting-and-remediating-malicious-updates/
tags:
- veille-cyber
- securelist
---
## Attaque par Compromission de la Chaîne d'Approvisionnement sur eScan Antivirus

Le 20 janvier, une attaque par compromission de la chaîne d'approvisionnement a ciblé le serveur de mise à jour de l'antivirus eScan. Le malware, un fichier nommé Reload.exe, a été distribué aux utilisateurs, initiant une chaîne d'infection. Ce fichier modifiait le fichier HOSTS pour bloquer les futures mises à jour légitimes, empêchant ainsi la correction automatique du problème et causant des erreurs de service. Le malware assurait également sa persistance via des tâches planifiées (ex: CorelDefrag) et téléchargeait des charges utiles supplémentaires. Un fichier nommé consctlx.exe était également déposé sur le disque.

Les attaquants ont réussi à accéder à un serveur de mise à jour régional et à y déployer le fichier malveillant, distribué avec une fausse signature numérique. Il est précisé qu'il ne s'agit pas d'une vulnérabilité mais d'un accès non autorisé à l'infrastructure.

**Points clés :**

*   **Type d'attaque :** Compromission de la chaîne d'approvisionnement (Supply Chain Attack).
*   **Cible :** Serveur de mise à jour de l'antivirus eScan.
*   **Malware principal :** Reload.exe.
*   **Méthode d'action du malware :** Modification du fichier HOSTS, établissement de persistance, téléchargement de charges utiles supplémentaires.
*   **Cause principale :** Accès non autorisé à un serveur de mise à jour régional.
*   **Défense initiale :** Solutions de sécurité de Kaspersky détectant le malware grâce à leur composant "Behavior Detection".

**Vulnérabilités exploitées (si applicable) :**

*   Aucune vulnérabilité logicielle spécifique n'est mentionnée. L'incident est décrit comme un **accès non autorisé à l'infrastructure**. Il n'y a pas de CVE associé dans l'article.

**Recommandations :**

*   **Détection :** Examiner les tâches planifiées pour des traces de malware, vérifier le fichier `C:\Windows\System32\drivers\etc\hosts` pour des domaines eScan bloqués, et analyser les journaux de mise à jour eScan du 20 janvier.
*   **Remédiation :** Les développeurs d'eScan ont mis à disposition un utilitaire spécifique pour supprimer le malware, annuler les modifications et restaurer la fonctionnalité de l'antivirus. Les clients peuvent le demander au support technique.
*   **Blocage :** Bloquer les adresses connues des serveurs de contrôle du malware.

**Indicateurs de Compromission (IoCs) :**

*   **Domaines :**
    *   vhs.delrosal[.]net
    *   tumama.hns[.]to
    *   blackice.sol-domain[.]org
    *   codegiant[.]io
    *   airanks.hns[.]to
    *   csc.biologii[.]net
*   **Fichiers :** Reload.exe, consctlx.exe.
*   **Tâches planifiées :** CorelDefrag (exemple).

---
[Source](https://securelist.com/escan-supply-chain-attack/118688/){:target="_blank"}
