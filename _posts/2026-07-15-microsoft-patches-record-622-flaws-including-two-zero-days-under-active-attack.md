---
title: 'Microsoft Patches Record 622 Flaws, Including Two Zero-Days Under Active Attack'
date: 2026-07-15
permalink: /posts/2026/07/15/microsoft-patches-record-622-flaws-including-two-zero-days-under-active-attack/
tags:
- veille-cyber
- hackernews
---
### Record historique de correctifs Microsoft : Priorité à la remédiation active

Microsoft a déployé son Patch Tuesday le plus volumineux à ce jour, corrigeant 622 vulnérabilités. Cette mise à jour massive, potentiellement liée à l'utilisation d'outils d'analyse par intelligence artificielle, rend la priorisation basée uniquement sur les scores de sévérité (CVSS) inefficace.

#### Vulnérabilités critiques sous exploitation active
Deux failles d'élévation de privilèges sont actuellement exploitées et doivent être traitées en priorité, indépendamment de leur score de criticité :

*   **CVE-2026-56164 (SharePoint Server) :** Permet à un attaquant non authentifié d'élever ses privilèges via le réseau. Aucune interaction utilisateur n'est requise.
*   **CVE-2026-56155 (Active Directory Federation Services) :** Permet à un utilisateur déjà authentifié d'élever ses privilèges localement via des contrôles d'accès défaillants.

#### Autres points clés
*   **BitLocker :** La faille **CVE-2026-50661** permet un contournement par accès physique, bien qu'elle ne soit pas actuellement exploitée.
*   **Fin du support :** SharePoint Server 2016 et 2019 atteignent la fin de leur support étendu, rendant le correctif du **CVE-2026-56164** particulièrement critique.
*   **Fin du protocole RC4 :** Microsoft finalise le durcissement de Kerberos en supprimant la possibilité de revenir en arrière sur la désactivation du protocole RC4.
*   **Chaîne d'attaques :** Le **CVE-2026-55040** (SharePoint) constitue une porte d'entrée pour des attaques RCE, dont une partie reste à corriger dans la mise à jour d'août.

#### Recommandations
1.  **Prioriser par l'exploitation :** Ne vous fiez pas aux scores CVSS. Donnez la priorité absolue aux vulnérabilités déjà marquées comme exploitées (CVE-2026-56164 et CVE-2026-56155).
2.  **Sécurisation SharePoint :** Activez l'AMSI (Antimalware Scan Interface) en mode "Full" sur les serveurs SharePoint pour atténuer les risques liés aux vulnérabilités de cette plateforme.
3.  **Migration Kerberos :** Avant de déployer les mises à jour, auditez vos comptes de service pour identifier ceux utilisant encore RC4. Modifiez les mots de passe des comptes flagués pour forcer la génération de clés AES, sous peine de ruptures d'authentification.
4.  **Processus de patching :** Réduisez le délai entre la publication et l'application des correctifs, car l'automatisation permet désormais aux attaquants de concevoir des exploits rapidement par comparaison binaire des correctifs.

---
[Source](https://thehackernews.com/2026/07/microsoft-patches-record-622-flaws.html){:target="_blank"}
