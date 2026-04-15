---
title: 'Microsoft Issues Patches for SharePoint Zero-Day and 168 Other New Vulnerabilities'
date: 2026-04-15
permalink: /posts/2026/04/15/microsoft-issues-patches-for-sharepoint-zero-day-and-168-other-new-vulnerabilities/
tags:
- veille-cyber
- hackernews
---
### Microsoft : Vague de correctifs massive incluant des vulnérabilités critiques et exploitées

Microsoft a publié une mise à jour corrective record traitant 169 failles de sécurité. Cette livraison inclut des correctifs pour des vulnérabilités critiques, des failles exploitées activement et des défauts de sécurité rendus publics avant leur résolution.

**Points clés :**
*   **Volume record :** Avec 169 CVE corrigées, il s'agit de la deuxième mise à jour la plus importante de l'histoire de Microsoft.
*   **Répartition des risques :** La majorité des failles concernent l'élévation de privilèges (93), suivies par l'exécution de code à distance (RCE) et la divulgation d'informations.
*   **Menace immédiate :** La CISA a intégré la faille SharePoint (CVE-2026-32201) à son catalogue des vulnérabilités connues exploitées (KEV), imposant une remédiation urgente.

**Vulnérabilités critiques et notables :**
*   **CVE-2026-32201 (Score 6.5) :** Vulnérabilité de type "spoofing" dans **SharePoint Server**, actuellement exploitée dans la nature. Elle permet à un attaquant de manipuler des contenus ou des interfaces pour tromper les utilisateurs.
*   **CVE-2026-33824 (Score 9.8) :** Faille RCE critique dans le service **Windows IKE (Internet Key Exchange)**. Cette vulnérabilité, très dangereuse car ne nécessitant aucune interaction utilisateur, expose les systèmes (notamment VPN/IPsec) à un compromis total.
*   **CVE-2026-33825 (Score 7.8) :** Faille d'élévation de privilèges dans **Microsoft Defender** (connue sous le nom de "BlueHammer"). Elle permettait à un attaquant local d'accéder aux secrets système (SAM) pour prendre le contrôle total de la machine.

**Recommandations :**
*   **Priorisation absolue :** Appliquer les correctifs en priorité sur les serveurs exposés à Internet, particulièrement ceux utilisant les services IKEv2 et Microsoft SharePoint.
*   **Déploiement rapide :** Respecter l'échéance du 28 avril 2026 imposée par la CISA pour les organismes fédéraux, une ligne directrice recommandée pour toutes les entreprises.
*   **Mise à jour automatique :** Vérifier que les mises à jour automatiques de Microsoft Defender sont bien actives, bien que le déploiement soit ici automatique, pour assurer une protection contre les variantes de l'exploit "BlueHammer".

---
[Source](https://thehackernews.com/2026/04/microsoft-issues-patches-for-sharepoint.html){:target="_blank"}
