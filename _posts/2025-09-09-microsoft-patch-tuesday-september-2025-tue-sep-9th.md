---
title: 'Microsoft Patch Tuesday September 2025, (Tue, Sep 9th)'
date: 2025-09-09
permalink: /posts/2025/09/09/microsoft-patch-tuesday-september-2025-tue-sep-9th/
tags:
- veille-cyber
- sans-isc
---
**Mise à jour de sécurité de septembre : 177 vulnérabilités corrigées**

Microsoft a publié ses correctifs de sécurité de septembre, traitant 177 vulnérabilités distinctes, dont 86 affectant ses propres produits. Aucune de ces failles n'a été exploitée avant cette publication, bien que deux aient été rendues publiques au préalable. Treize de ces vulnérabilités sont considérées comme critiques. Des correctifs sont également disponibles pour des distributions Linux comme Mariner et Azure Linux, bien que leur criticité n'ait pas été systématiquement indiquée.

**Points clés et vulnérabilités notables :**

*   **CVE-2025-54107, CVE-2025-54917 (MapUrlToZone Security Feature Bypass) :** Permet à un attaquant de contourner des fonctionnalités de sécurité en manipulant la classification des URL dans différentes zones de sécurité (Intranet, Internet). La gravité est jugée importante, avec un score CVSS de 4.3.
*   **CVE-2025-55226, CVE-2025-55236 (Graphics Kernel Remote Code Execution) :** Bien qualifiées de "exécution de code à distance", ces vulnérabilités permettraient à un attaquant autorisé d'exécuter du code localement. L'interprétation suggère qu'un utilisateur pourrait déclencher le code involontairement en visualisant une image. Leur gravité est critique, avec des scores CVSS de 6.7 et 7.3 respectivement.
*   **Vulnérabilités critiques dans Azure et les services Microsoft :** Plusieurs vulnérabilités critiques ont été identifiées dans Azure Bot Service (CVE-2025-55244), Azure Entra (CVE-2025-55241) et Azure Networking (CVE-2025-54914), offrant des élévations de privilèges.
*   **Exécution de code à distance et divulgation d'informations :** Diverses vulnérabilités affectent des produits comme Microsoft Excel (plusieurs CVE), Microsoft Office (CVE-2025-54910), Microsoft SQL Server (CVE-2025-47997), et les composants graphiques de Windows (CVE-2025-54919, CVE-2025-55228).

**Recommandations :**

Aucune vulnérabilité ne nécessite une action immédiate ("patch now") selon l'analyse. Il est recommandé d'appliquer les correctifs conformément à la politique de gestion des vulnérabilités locale, idéalement avant le prochain cycle de mises à jour.

---
[Source](https://isc.sans.edu/diary/rss/32270){:target="_blank"}
