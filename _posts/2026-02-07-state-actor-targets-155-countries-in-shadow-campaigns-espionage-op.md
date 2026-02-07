---
title: 'State actor targets 155 countries in Shadow Campaigns espionage op'
date: 2026-02-07
permalink: /posts/2026/02/07/state-actor-targets-155-countries-in-shadow-campaigns-espionage-op/
tags:
- veille-cyber
- bleepingcomp
---
## Campagne d'espionnage "Shadow Campaigns" : Une Menace Mondiale

Une opération d'espionnage à l'échelle mondiale, baptisée "Shadow Campaigns", a ciblé des réseaux gouvernementaux et d'infrastructures critiques dans 37 pays, avec des activités de reconnaissance étendues touchant 155 pays. Ce groupe de menace parrainé par un État, actif depuis janvier 2024 et vraisemblablement basé en Asie, est suivi sous la désignation TGR-STA-1030/UNC6619. Les cibles principales incluent les ministères, les forces de l'ordre, le contrôle des frontières, les finances, le commerce, l'énergie, l'immigration et les agences diplomatiques.

### Points Clés :

*   **Portée étendue :** Au moins 70 organisations gouvernementales et d'infrastructures critiques ont été compromises dans 37 pays. L'activité de reconnaissance a touché des entités liées à 155 pays.
*   **Motivations :** La campagne semble axée sur la collecte de renseignements stratégiques, économiques et politiques. Des pics d'activité ont été observés en corrélation avec des événements géopolitiques spécifiques, comme la période de fermeture du gouvernement américain et les élections nationales au Honduras.
*   **Méthodologies :** Le groupe utilise des emails de phishing sophistiqués pour obtenir un accès initial, souvent liés à des réorganisations internes. Les liens contenus dans ces emails mènent à des archives malveillantes hébergées sur des services de stockage en ligne.
*   **Outils avancés :** Outre les techniques de phishing, le groupe exploite au moins 15 vulnérabilités connues dans des systèmes tels que SAP Solution Manager, Microsoft Exchange Server, D-Link et Microsoft Windows. Un rootkit Linux eBPF personnalisé, nommé "ShadowGuard", a été découvert, permettant de masquer des processus et des données au niveau du noyau.

### Vulnérabilités :

L'article mentionne l'exploitation de vulnérabilités dans les produits suivants, mais ne précise pas de CVE spécifiques :

*   SAP Solution Manager
*   Microsoft Exchange Server
*   D-Link
*   Microsoft Windows

### Recommandations :

Bien que l'article ne liste pas de recommandations formelles, les points suivants peuvent être déduits pour la défense :

*   **Vigilance accrue face au phishing :** Former les employés à identifier et signaler les emails suspects, en particulier ceux mentionnant des réorganisations internes ou des lueurs similaires.
*   **Application des correctifs :** Maintenir les systèmes à jour en appliquant rapidement les correctifs pour les vulnérabilités connues, en particulier pour les logiciels mentionnés (SAP, Microsoft Exchange, etc.).
*   **Renforcement de la sécurité du réseau :** Mettre en place des mesures de détection et de prévention des intrusions robustes pour identifier les activités suspectes et les tentatives d'accès non autorisé.
*   **Surveillance approfondie des journaux :** Surveiller attentivement les journaux système et de sécurité, en particulier pour détecter les activités inhabituelles au niveau du noyau Linux qui pourraient indiquer l'utilisation de rootkits.
*   **Utilisation d'outils de sécurité avancés :** Déployer des solutions de sécurité capables de détecter des menaces sophistiquées, y compris des techniques d'évasion d'analyse et des rootkits avancés.

---
[Source](https://www.bleepingcomputer.com/news/security/state-actor-targets-155-countries-in-shadow-campaigns-espionage-op/){:target="_blank"}
