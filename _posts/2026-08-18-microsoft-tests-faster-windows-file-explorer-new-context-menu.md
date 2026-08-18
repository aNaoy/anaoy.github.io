---
title: 'Microsoft tests faster Windows File Explorer, new context menu'
date: 2026-08-18
permalink: /posts/2026/08/18/microsoft-tests-faster-windows-file-explorer-new-context-menu/
tags:
- veille-cyber
- bleepingcomp
---
### Optimisation de l'Explorateur Windows et suppression d'un vecteur d'attaque

Microsoft déploie actuellement auprès des utilisateurs du programme Insider des améliorations significatives pour l'Explorateur de fichiers de Windows 11, visant à accroître sa réactivité, sa fiabilité et sa personnalisation. Parallèlement, l'éditeur renforce la sécurité du système en supprimant un outil fréquemment détourné par des cybercriminels.

**Points clés des mises à jour :**
* **Performances :** Optimisation globale de la vitesse de l'Explorateur et élimination des interruptions lors du renommage de fichiers causées par la synchronisation en arrière-plan.
* **Interface :** Refonte du menu contextuel (clic droit) pour le rendre plus épuré et davantage personnalisable via un nouveau panneau dans les paramètres.
* **Préchargement :** Poursuite des tests de préchargement en arrière-plan pour accélérer le lancement de l'Explorateur.

**Vulnérabilité adressée :**
* **WMIC (Windows Management Instrumentation Command-line) :** Microsoft officialise la suppression de cet utilitaire à partir de Windows 11 24H2 et 25H2. WMIC est classé comme un **LOLBIN** (*Living-off-the-Land Binary*), un outil système légitime détourné par les attaquants pour exécuter des commandes malveillantes, contourner la détection et maintenir une persistance sans introduire de logiciels tiers.

**Recommandations :**
* **Migration :** Les administrateurs systèmes et les développeurs utilisant encore WMIC doivent migrer leurs scripts et processus vers **PowerShell**, qui remplace cet outil de manière plus sécurisée.
* **Mise à jour :** Planifier la transition vers les versions 24H2 ou 25H2 de Windows 11 pour bénéficier de la suppression de cette surface d'attaque et des optimisations de performance.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-tests-faster-windows-explorer-customizable-context-menu/){:target="_blank"}
