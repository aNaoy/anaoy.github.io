---
title: 'Microsoft Teams vishing attacks lead to Chaos ransomware attacks'
date: 2026-07-30
permalink: /posts/2026/07/30/microsoft-teams-vishing-attacks-lead-to-chaos-ransomware-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vishing sur Microsoft Teams : la campagne STAC4749 et le ransomware Chaos

Des cyberattaquants, identifiés sous le nom de code **STAC4749**, mènent des campagnes de *vishing* (hameçonnage vocal) via Microsoft Teams en usurpant l'identité du support informatique pour infiltrer des entreprises nord-américaines. Ces intrusions mènent, dans certains cas, au déploiement du ransomware **Chaos** en moins de 17 heures.

**Points clés :**
* **Mode opératoire :** Les attaquants contactent des employés via Teams (appels audio/chat) en utilisant des domaines trompeurs (ex: *supportsoft[.]top*).
* **Technique d'accès :** Convaincre les victimes d'utiliser des outils de prise de contrôle à distance légitimes, principalement **Microsoft Quick Assist** ou **RemSupp**.
* **Persistance :** Installation de portes dérobées (backdoors) dissimulées sous des noms de composants audio (Realtek/Windows) et utilisation d'outils comme DWAgent ou AnyDesk.
* **Mouvement latéral :** Activation du protocole RDP pour compromettre d'autres systèmes sur le réseau.
* **Ciblage :** Secteurs des services, de l'énergie, de la construction et de l'ingénierie (principalement au Canada et aux États-Unis).

**Vulnérabilités exploitées :**
* L'attaque ne repose pas sur une vulnérabilité logicielle (CVE) spécifique, mais sur l'ingénierie sociale et l'abus de fonctionnalités légitimes de gestion à distance (Living-off-the-land).

**Recommandations :**
* **Sensibilisation :** Former les employés à ne jamais accorder un accès à distance à un "support technique" contactant l'entreprise via des comptes externes sur Teams.
* **Gestion des accès :** Restreindre l'utilisation des outils de prise de contrôle à distance (Quick Assist, RemSupp, AnyDesk) aux seules solutions validées et gérées par le département IT interne.
* **Filtrage réseau :** Bloquer les domaines suspects ou récemment créés (.top) et surveiller l'installation d'outils de gestion à distance non autorisés.
* **Monitoring EDR :** Surveiller les processus suspects dans les dossiers `%AppData%` et la création de services de persistance imitant des pilotes audio ou des composants système Windows.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-teams-vishing-attacks-lead-to-chaos-ransomware-attacks/){:target="_blank"}
