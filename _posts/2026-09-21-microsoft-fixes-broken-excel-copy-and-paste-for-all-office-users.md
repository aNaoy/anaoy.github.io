---
title: 'Microsoft fixes broken Excel copy and paste for all Office users'
date: 2026-09-21
permalink: /posts/2026/09/21/microsoft-fixes-broken-excel-copy-and-paste-for-all-office-users/
tags:
- veille-cyber
- bleepingcomp
---
### Correctif Microsoft pour les dysfonctionnements du copier-coller dans Excel

Suite au déploiement des mises à jour de sécurité de septembre 2026 (notamment la mise à jour KB5002914), de nombreux utilisateurs de Microsoft Excel ont rencontré des échecs silencieux lors des opérations de copier-coller, de remplissage automatique ou de glissement de formules.

**Points clés :**
* Le bug touche les versions 2016, 2019, 2021, 2024 d'Excel ainsi qu'Office Online Server.
* L'échec se manifeste sans aucun message d'erreur ni signal sonore, laissant la source sélectionnée et la destination inchangée.
* Aucun CVE n'a été associé à ce bug fonctionnel, car il s'agit d'une régression logicielle introduite par une mise à jour de sécurité et non d'une vulnérabilité exploitée.

**Recommandations :**
* **Installation de correctifs :** Appliquer manuellement les mises à jour spécifiques fournies par Microsoft pour chaque version concernée :
    * **Office 2016 :** KB5002665
    * **Office LTSC 2019 :** Build 10417.20208
    * **Office LTSC 2021 :** Build 14334.20918
    * **Office LTSC 2024 :** Build 17932.21000
* **Contournement temporaire :** Pour les fichiers contenant de la mise en forme conditionnelle où le problème persiste, utiliser la fonction « Collage spécial » (via le raccourci `Ctrl+Alt+V`) pour sélectionner un mode de collage spécifique (valeurs, formules, etc.).

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-broken-excel-copy-and-paste-for-all-office-users/){:target="_blank"}
