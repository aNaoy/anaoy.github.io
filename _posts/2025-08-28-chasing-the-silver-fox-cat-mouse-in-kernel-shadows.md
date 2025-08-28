---
title: 'Chasing the Silver Fox: Cat & Mouse in Kernel Shadows'
date: 2025-08-28
permalink: /posts/2025/08/28/chasing-the-silver-fox-cat-mouse-in-kernel-shadows/
tags:
- veille-cyber
- zerodaysfans
---
### Exploitation de Drivers Signés pour Éviter les Protections

Une campagne active menée par le groupe APT Silver Fox utilise des drivers signés et vulnérables pour contourner les solutions de sécurité sur les systèmes Windows. L'objectif principal est de neutraliser les processus de sécurité, y compris ceux protégés par les mécanismes PP/PPL, afin de faciliter le déploiement de leur malware, le RAT ValleyRAT.

**Points Clés :**

*   **Utilisation de Drivers Inconnus et Signés :** La campagne exploite le driver `amsdk.sys` (WatchDog Antimalware, version 1.0.600), signé par Microsoft et non répertorié dans les listes de blocage de drivers vulnérables. Cela permet l'évasion des défenses basées sur les signatures et la confiance.
*   **Stratégie à Double Driver :** Pour assurer la compatibilité, un driver Zemana connu pour ses vulnérabilités est utilisé pour les systèmes plus anciens, tandis que le driver WatchDog est employé pour les environnements modernes.
*   **Évasion Sophistiquée :** Après la publication des vulnérabilités, les attaquants ont adapté le driver corrigé en modifiant un seul octet dans le champ de timestamp non authentifié de la signature numérique. Cette technique permet de conserver une signature Microsoft valide tout en changeant le hachage du fichier, contournant ainsi les listes de blocage basées sur les hachages.
*   **Charge Utile Finale :** Le RAT ValleyRAT, un cheval de Troie d'accès à distance attribuable à Silver Fox APT et dont l'infrastructure est située en Chine, est la charge utile finale dans toutes les variantes observées.
*   **Loader Tout-en-Un :** Les échantillons analysés sont des chargeurs autonomes intégrant des couches anti-analyse, les drivers vulnérables, la logique d'élimination des EDR/AV et le module de téléchargement de ValleyRAT.

**Vulnérabilités :**

*   **`amsdk.sys` (WatchDog Antimalware, version 1.0.600)**
    *   **Description :** Le driver permet l'arrêt arbitraire de processus, y compris des processus protégés (PP/PPL). La vulnérabilité principale réside dans l'utilisation de `IoCreateDeviceSecure` sans le flag `FILE_DEVICE_SECURE_OPEN`, ce qui permet à des utilisateurs non privilégiés d'accéder au namespace du driver, contournant ainsi le DACL strict appliqué.
    *   **Impact :** Local Privilege Escalation (LPE) et capacité à terminer des processus de sécurité (EDR/AV) pour contourner les protections.
    *   **IOCTLs exploitées :** `IOCTL_REGISTER_PROCESS` (0x80002010), `IOCTL_TERMINATE_PROCESS` (0x80002048).
    *   **CVE :** Non spécifié dans l'article, mais l'exploitation est comparée à des vulnérabilités connues dans les drivers Zemana.

*   **Driver Advanced Malware Protection (`ZAM.exe`, version 3.0.0.000)**
    *   **Description :** Driver historiquement connu pour ses vulnérabilités permettant l'arrêt arbitraire de processus.
    *   **Impact :** Désactivation des solutions de sécurité.

**Recommandations :**

*   **Application de la Blocklist de Drivers Vulnérables :** Appliquer manuellement les mises à jour de la liste de blocage des drivers vulnérables de Microsoft, car les mises à jour automatiques peuvent être espacées.
*   **Détection Basée sur le Comportement :** Mettre en œuvre des mécanismes de détection basés sur le comportement et l'heuristique pour identifier l'abus de drivers légitimes, même s'ils sont signés.
*   **Surveillance et Prévention :** Surveiller et prévenir l'utilisation de drivers vulnérables connus et de leurs variantes, potentiellement à l'aide de règles YARA (fournies dans l'article).
*   **Mise à Jour des Solutions de Sécurité :** S'assurer que les solutions de sécurité sont à jour pour bénéficier des correctifs des vulnérabilités de drivers connues et des nouvelles signatures.
*   **Examen Approfondi des Drivers Signés :** Examiner de plus près les drivers signés, même ceux considérés comme fiables, pour détecter des comportements anormaux ou des vulnérabilités latentes.
*   **Correction des Drivers :** Les éditeurs de logiciels doivent s'assurer que leurs drivers sont correctement sécurisés, en implémentant des DACL stricts et le flag `FILE_DEVICE_SECURE_OPEN`, et en effectuant des vérifications rigoureuses sur les processus protégés (PP/PPL) avant leur manipulation.

La campagne met en évidence la tendance croissante à l'exploitation de drivers signés mais vulnérables pour contourner les défenses des terminaux et échapper à la détection statique. La capacité des attaquants à modifier rapidement des composants corrigés pour contourner les blocages basés sur les hachages souligne la nécessité d'une vigilance continue et de stratégies de défense multicouches.

---
[Source](https://research.checkpoint.com/2025/silver-fox-apt-vulnerable-drivers/){:target="_blank"}
