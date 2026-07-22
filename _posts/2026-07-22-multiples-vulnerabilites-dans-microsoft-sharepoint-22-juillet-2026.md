---
title: 'Multiples vulnérabilités dans Microsoft Sharepoint (22 juillet 2026)'
date: 2026-07-22
permalink: /posts/2026/07/22/multiples-vulnerabilites-dans-microsoft-sharepoint-22-juillet-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilités critiques d'exécution de code dans Microsoft SharePoint

Microsoft a publié des correctifs pour deux vulnérabilités critiques affectant plusieurs versions de SharePoint, permettant à un attaquant non authentifié d'exécuter du code arbitraire à distance (RCE). Ces failles font l'objet d'exploitations actives et de preuves de concept (PoC) publiques.

**Vulnérabilités identifiées :**
*   **CVE-2026-58644 :** Vulnérabilité RCE activement exploitée.
*   **CVE-2026-50522 :** Vulnérabilité RCE pour laquelle des preuves de concept publiques et des exploitations actives ont été rapportées.

**Systèmes affectés :**
*   Microsoft SharePoint Enterprise Server 2016.
*   Microsoft SharePoint Server 2019.
*   Microsoft SharePoint Server Subscription Edition.
*(Versions antérieures aux correctifs listés dans les bulletins de sécurité officiels).*

**Points clés :**
*   Le risque est maximal : les attaquants ne nécessitent aucune authentification pour prendre le contrôle des serveurs.
*   La disponibilité de preuves de concept augmente considérablement le risque d'attaques généralisées.

**Recommandations :**
*   **Application immédiate :** Déployer les correctifs de sécurité fournis par Microsoft sans délai.
*   **Gestion des secrets :** En cas de suspicion de compromission, procéder impérativement à une rotation des clés de machine ASP.NET et des autres secrets sensibles, afin d'empêcher la persistance d'un attaquant après l'application des correctifs.

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-008/){:target="_blank"}
